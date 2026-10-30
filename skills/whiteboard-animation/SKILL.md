---
name: whiteboard-animation
description: Turn finished pictures into hand-drawn whiteboard animation videos with the Whiteboard Animation MCP tools. Use when the user asks for a whiteboard animation, a hand-drawn or sketch-style reveal of an image, a doodle video, or to animate a diagram, illustration, product shot or folder of pictures as if drawn by hand.
---

# Whiteboard Animation

The `whiteboard-animation` MCP server (`https://mcp.whiteboardanimation.ai/mcp`) draws a finished picture stroke by stroke, sketch first and then colour, optionally with a hand, and renders it as MP4, transparent WebM or PNG.

If its tools are not available, tell the user how to add the server (see the repository README) and stop.

## Flow

1. **`status`** first: confirms the sign-in and shows credits left and how many drawings may queue. If it asks for sign-in, have the user finish it in their client.
2. **`quote`**: tell the user what each drawing costs before spending credits on several.
3. **Get the picture in.**
   - In ChatGPT, pass the attached file to `create_drawing` as `image`.
   - Elsewhere call `create_upload` with the file name, content type and size, `PUT` the bytes to `upload_url` with the returned headers, then pass `upload_id` to `create_drawing`.
4. **`create_drawing`** answers at once with a `drawing_id`. A drawing takes a few minutes. Retrying with the same picture and choices returns the same drawing, so a retry never charges twice.
5. **Follow it** with `get_drawing` (or `wait_drawing`, which answers as soon as it moves on). Share the preview page link while it draws.
6. **Export** with `render_link`: one link for up to 20 drawings, each with its own format, resolution, aspect, background and hand (read the options from `get_drawing`). Opening the link in a browser renders the files into that browser's downloads. Follow it with `wait_render` until every file is `saved`.

## Rules

- It draws a picture the user already has; it does not make one from text. If the user has no picture, suggest making one first with an image tool.
- Ask before drawing many pictures at once, with the total from `quote`.
- For a folder of pictures, upload and create all drawings first, then make one `render_link` for all of them, and move the saved files where the user wants them.

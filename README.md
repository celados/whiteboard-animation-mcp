<p align="center">
  <a href="https://whiteboardanimation.ai/mcp"><img src="assets/logo.svg" alt="Whiteboard Animation" width="88" height="88"></a>
</p>

<h1 align="center">Whiteboard Animation MCP Server</h1>

<p align="center">
  <b>Hand your AI assistant a picture. Get it back as a hand-drawn whiteboard animation.</b><br>
  The official remote MCP server for <a href="https://whiteboardanimation.ai">WhiteboardAnimation.ai</a>: works in Claude, ChatGPT, Cursor, VS Code, Codex and any MCP client.
</p>

<p align="center">
  <a href="https://registry.modelcontextprotocol.io/v0.1/servers?search=ai.whiteboardanimation"><img src="assets/badges/mcp-registry.svg" alt="MCP Registry"></a>
  <img src="assets/badges/streamable-http.svg" alt="Streamable HTTP">
  <img src="assets/badges/oauth-2-1.svg" alt="OAuth 2.1">
  <img src="assets/badges/no-api-key.svg" alt="No API key">
  <a href="LICENSE"><img src="assets/badges/mit.svg" alt="MIT"></a>
</p>

<p align="center">
  <a href="https://whiteboardanimation.ai/mcp"><b>Website</b></a> ·
  <a href="#one-click-setup"><b>Setup</b></a> ·
  <a href="#what-to-ask-for"><b>Examples</b></a> ·
  <a href="#tools"><b>Tools</b></a> ·
  <a href="#faq"><b>FAQ</b></a>
</p>

<p align="center">
  <img src="assets/demo.gif" alt="A fox at a pond, drawn stroke by stroke by a hand, sketched first and then coloured in" width="720">
</p>

The server is hosted at **`https://mcp.whiteboardanimation.ai/mcp`**. There is nothing to install and no key to paste: connect it once, sign in with your WhiteboardAnimation.ai account, and ask your assistant to draw any finished picture. It sketches the picture stroke by stroke, colours it in, shows the drawing right in the chat, and hands you a link that saves the MP4. New accounts start with free credits.

## One-click setup

<table>
  <tr>
    <td align="center" width="25%">
      <a href="https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Whiteboard%20Animation&connectorUrl=https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp"><img src="assets/badges/add-to-claude.svg" alt="Add to Claude"></a>
      <br><sub>Claude on the web and desktop.<br>Fills in the custom connector.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://chatgpt.com/plugins"><img src="assets/badges/add-to-chatgpt.svg" alt="Add to ChatGPT"></a>
      <br><sub>Plugins → <b>+</b> → Add custom MCP server,<br>then paste the address.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://cursor.com/en/install-mcp?name=whiteboard-animation&config=eyJ1cmwiOiJodHRwczovL21jcC53aGl0ZWJvYXJkYW5pbWF0aW9uLmFpL21jcCJ9"><img src="assets/badges/add-to-cursor.svg" alt="Add to Cursor"></a>
      <br><sub>Installs into Cursor;<br>sign in from Settings → MCP.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://vscode.dev/redirect/mcp/install?name=whiteboard-animation&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp%22%7D"><img src="assets/badges/add-to-vs-code.svg" alt="Add to VS Code"></a>
      <br><sub>Or <a href="https://insiders.vscode.dev/redirect/mcp/install?name=whiteboard-animation&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp%22%7D">VS Code Insiders</a>.<br>Start it and sign in.</sub>
    </td>
  </tr>
</table>

### Or let your agent do it

Paste this into Claude Code, Codex, Cursor or any agent that can edit its own MCP settings:

```text
Add the Whiteboard Animation MCP server to my MCP settings: streamable HTTP at https://mcp.whiteboardanimation.ai/mcp, sign-in with OAuth (no API key). Then help me sign in, and once it is connected, call its status tool and tell me how many credits I have.
```

### By hand

<details>
<summary><b>ChatGPT</b></summary>

1. Open [Plugins](https://chatgpt.com/plugins) in ChatGPT on the web.
2. Choose **+ → Add custom MCP server**, name it `Whiteboard Animation`, paste `https://mcp.whiteboardanimation.ai/mcp` and choose **OAuth**.
3. Tick the risk notice, choose **Create as a plugin** and sign in with your WhiteboardAnimation.ai account.
4. In a chat, attach a picture and ask for a whiteboard animation.

</details>

<details>
<summary><b>Claude</b> (web and desktop)</summary>

1. Open **Customize → Connectors** and add a custom connector named `Whiteboard Animation` with `https://mcp.whiteboardanimation.ai/mcp`, or use the [Add to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Whiteboard%20Animation&connectorUrl=https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp) button.
2. Choose **Connect** and sign in with your WhiteboardAnimation.ai account.
3. Give Claude a finished picture and ask for a whiteboard animation.

</details>

<details>
<summary><b>Claude Code</b></summary>

As an MCP server:

```sh
claude mcp add --transport http whiteboard-animation https://mcp.whiteboardanimation.ai/mcp
```

Or as a plugin, which adds the server and a skill that knows the whole flow:

```text
/plugin marketplace add celados/whiteboard-animation-mcp
/plugin install whiteboard-animation@whiteboard-animation
```

Then run `/mcp`, choose `whiteboard-animation` and sign in.

</details>

<details>
<summary><b>Cursor</b></summary>

Use the [Add to Cursor](https://cursor.com/en/install-mcp?name=whiteboard-animation&config=eyJ1cmwiOiJodHRwczovL21jcC53aGl0ZWJvYXJkYW5pbWF0aW9uLmFpL21jcCJ9) button, or put this in `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "whiteboard-animation": { "url": "https://mcp.whiteboardanimation.ai/mcp" }
  }
}
```

Sign in when Cursor asks, from **Settings → MCP**.

</details>

<details>
<summary><b>VS Code</b></summary>

Use the [Add to VS Code](https://vscode.dev/redirect/mcp/install?name=whiteboard-animation&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp%22%7D) button, or run:

```sh
code --add-mcp '{"name":"whiteboard-animation","type":"http","url":"https://mcp.whiteboardanimation.ai/mcp"}'
```

Start it from the MCP servers list and sign in when asked.

</details>

<details>
<summary><b>Codex</b></summary>

```sh
codex mcp add whiteboard-animation --url https://mcp.whiteboardanimation.ai/mcp
codex mcp login whiteboard-animation
```

</details>

<details>
<summary><b>Gemini CLI</b></summary>

```sh
gemini extensions install https://github.com/celados/whiteboard-animation-mcp
```

</details>

<details>
<summary><b>Any other MCP client</b></summary>

Any client that speaks streamable HTTP and OAuth connects with `https://mcp.whiteboardanimation.ai/mcp`. Sign-in uses dynamic client registration, so the client registers itself.

</details>

## How it works

<table>
  <tr>
    <td width="33%"><img src="assets/step-connect.webp" alt="Connect it"></td>
    <td width="33%"><img src="assets/step-sign-in.webp" alt="Sign in once"></td>
    <td width="33%"><img src="assets/step-draw.webp" alt="Hand it a picture"></td>
  </tr>
  <tr>
    <td valign="top"><b>1. Connect it.</b> One click in Claude, Cursor or VS Code, or from ChatGPT's Plugins page. Coding agents add it themselves from the setup prompt.</td>
    <td valign="top"><b>2. Sign in once.</b> With your WhiteboardAnimation.ai account, over OAuth. Nothing to copy, and you can disconnect any time.</td>
    <td valign="top"><b>3. Hand it a picture.</b> Your assistant draws it stroke by stroke, shows the drawing in the chat and gives you a link that saves the video.</td>
  </tr>
</table>

## What to ask for

<table>
  <tr>
    <td width="50%"><img src="assets/use-lesson.webp" alt="A lesson explainer"></td>
    <td width="50%"><img src="assets/use-product.webp" alt="A product reveal"></td>
  </tr>
  <tr>
    <td valign="top"><b>A lesson explainer</b><br><sub>“Turn my diagram into a whiteboard animation for a lesson: draw the subject first with a right hand.”</sub></td>
    <td valign="top"><b>A product reveal</b><br><sub>“Draw my product picture as a whiteboard animation, the product first and the background after, then give me the link that saves the MP4.”</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="assets/use-book.webp" alt="A picture-book page"></td>
    <td width="50%"><img src="assets/use-folder.webp" alt="A folder of scenes"></td>
  </tr>
  <tr>
    <td valign="top"><b>A picture-book page</b><br><sub>“Turn each page of my picture book into a whiteboard animation, one drawing per page, and tell me when all of them are done.”</sub></td>
    <td valign="top"><b>A folder of scenes</b><br><sub>“Draw every picture in ./scenes as a whiteboard animation, then open one render link for all of them as MP4 and move the saved files to ./clips.”</sub></td>
  </tr>
</table>

## Tools

| Tool | What it does |
| --- | --- |
| `status` | The signed-in account: plan, credits left, drawings queued and running. |
| `quote` | What one drawing costs in credits, and the quote to pass when creating it. |
| `create_upload` | Reserves an upload and answers a URL to `PUT` the picture to. |
| `create_drawing` | Draws a picture as a whiteboard animation (spends credits). Answers at once with the drawing id. |
| `get_drawing` | A drawing's status and progress, its preview page, and its export options once done. |
| `wait_drawing` | Waits until a drawing moves on, so the in-chat card can follow it live. |
| `list_drawings` | The latest drawings in your library. |
| `render_link` | One link that renders up to 20 drawings as MP4, transparent WebM or PNG, each with its own options. |
| `wait_render` | Follows a render link until each file is saved. |

Only `create_upload` and `create_drawing` write anything; nothing deletes. In Claude and ChatGPT the drawing plays in an interactive card inside the chat.

## FAQ

**Do I need an API key?**
No. You sign in once with your WhiteboardAnimation.ai account (OAuth 2.1) and the client keeps you signed in. Disconnect the connector to stop it.

**Can it make a picture from a text prompt?**
No. Bring a finished picture: make it first with an image tool, in the same chat if you like, then ask for the whiteboard animation.

**Does it give me a video file?**
It gives you a link: opened in any browser, the page renders the MP4 or WebM and saves it to your downloads. A coding agent can open it for you and move the files where you want them.

**What does it cost?**
New accounts start with free credits. After that, see [pricing](https://whiteboardanimation.ai/pricing).

**Is the server open source?**
No. The server is a hosted service; this repository holds its public listing, the client configs and the agent skill. Issues and questions are welcome here.

## Links

- [WhiteboardAnimation.ai/mcp](https://whiteboardanimation.ai/mcp): the MCP page, with setup for every client
- [Official MCP Registry entry](https://registry.modelcontextprotocol.io/v0.1/servers?search=ai.whiteboardanimation): `ai.whiteboardanimation/whiteboard-animation`
- [Privacy](https://whiteboardanimation.ai/privacy) · [Terms](https://whiteboardanimation.ai/terms) · [hello@whiteboardanimation.ai](mailto:hello@whiteboardanimation.ai)

## License

The configs, skill and docs in this repository are [MIT](LICENSE). The hosted service is covered by the [WhiteboardAnimation.ai terms](https://whiteboardanimation.ai/terms).

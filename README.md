<p align="center">
  <a href="https://whiteboardanimation.ai/mcp"><img src="assets/logo.svg" alt="Whiteboard Animation" width="88" height="88"></a>
</p>

<h1 align="center">Whiteboard Animation MCP Server</h1>

<p align="center">
  <b>Hand your AI assistant a picture. Get it back as a hand-drawn whiteboard animation.</b><br>
  The official remote MCP server for <a href="https://whiteboardanimation.ai">WhiteboardAnimation.ai</a>: works in Claude, ChatGPT, Cursor, VS Code, Codex and any MCP client.
</p>

<p align="center">
  <a href="https://registry.modelcontextprotocol.io/v0.1/servers?search=ai.whiteboardanimation"><img src="https://img.shields.io/badge/MCP_Registry-ai.whiteboardanimation-111111?logo=modelcontextprotocol&logoColor=white" alt="MCP Registry"></a>
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-111111" alt="Streamable HTTP">
  <img src="https://img.shields.io/badge/Auth-OAuth_2.1-C8462B" alt="OAuth 2.1">
  <img src="https://img.shields.io/badge/API_key-not_needed-C8462B" alt="No API key">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/celados/whiteboard-animation-mcp?color=111111" alt="MIT"></a>
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
      <a href="https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Whiteboard%20Animation&connectorUrl=https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp"><img src="https://img.shields.io/badge/Add%20to%20Claude-D97757?style=for-the-badge&logo=claude&logoColor=white" alt="Add to Claude"></a>
      <br><sub>Claude on the web and desktop.<br>Fills in the custom connector.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://chatgpt.com/plugins"><img src="https://img.shields.io/badge/Add%20to%20ChatGPT-10A37F?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0iI2ZmZmZmZiI%2BPHBhdGggZD0iTTIwLjU2MiAxMC4xODhjLjI1LS42ODguMzEzLTEuMzc2LjI1LTIuMDYzYy0uMDYyLS42ODctLjMxMi0xLjM3NS0uNjI1LTJjLS41NjItLjkzNy0xLjM3NS0xLjY4Ny0yLjMxMi0yLjEyNWMtMS0uNDM3LTIuMDYzLS41NjItMy4xMjUtLjMxMmMtLjUtLjUtMS4wNjMtLjkzOC0xLjY4OC0xLjI1UzExLjY4NyAyIDExIDJhNS4xNyA1LjE3IDAgMCAwLTMgLjkzOGMtLjg3NS42MjQtMS41IDEuNS0xLjgxMyAyLjVjLS43NS4xODctMS4zNzUuNS0yIC44NzVjLS41NjIuNDM3LTEgMS0xLjM3NSAxLjU2MmMtLjU2Mi45MzgtLjc1IDItLjYyNSAzLjA2M2E1LjQ0IDUuNDQgMCAwIDAgMS4yNSAyLjg3NGE0LjcgNC43IDAgMCAwLS4yNSAyLjA2M2MuMDYzLjY4OC4zMTMgMS4zNzUuNjI1IDJjLjU2My45MzggMS4zNzUgMS42ODggMi4zMTMgMi4xMjVjMSAuNDM4IDIuMDYyLjU2MyAzLjEyNS4zMTNjLjUuNSAxLjA2Mi45MzcgMS42ODcgMS4yNVMxMi4zMTIgMjIgMTMgMjJhNS4xNyA1LjE3IDAgMCAwIDMtLjkzN2MuODc1LS42MjUgMS41LTEuNSAxLjgxMi0yLjVhNC41NCA0LjU0IDAgMCAwIDEuOTM4LS44NzVjLjU2Mi0uNDM4IDEuMDYyLS45MzggMS4zNzUtMS41NjNjLjU2Mi0uOTM3Ljc1LTIgLjYyNS0zLjA2MmMtLjEyNS0xLjA2My0uNS0yLjA2My0xLjE4OC0yLjg3Nm0tNy41IDEwLjVjLTEgMC0xLjc1LS4zMTMtMi40MzctLjg3NWMwIDAgLjA2Mi0uMDYzLjEyNS0uMDYzbDQtMi4zMTJhLjUuNSAwIDAgMCAuMjUtLjI1YS41Ny41NyAwIDAgMCAuMDYyLS4zMTNWMTEuMjVsMS42ODggMXY0LjYyNWEzLjY4NSAzLjY4NSAwIDAgMS0zLjY4OCAzLjgxM001IDE3LjI1Yy0uNDM4LS43NS0uNjI1LTEuNjI1LS40MzgtMi41YzAgMCAuMDYzLjA2My4xMjUuMDYzbDQgMi4zMTJhLjU2LjU2IDAgMCAwIC4zMTMuMDYzYy4xMjUgMCAuMjUgMCAuMzEyLS4wNjNsNC44NzUtMi44MTJ2MS45MzdsLTQuMDYyIDIuMzc1QTMuNyAzLjcgMCAwIDEgNy4zMTIgMTljLTEtLjI1LTEuODEyLS44NzUtMi4zMTItMS43NU0zLjkzNyA4LjU2M2EzLjggMy44IDAgMCAxIDEuOTM4LTEuNjI2djQuNzUxYzAgLjEyNCAwIC4yNS4wNjIuMzEyYS41LjUgMCAwIDAgLjI1LjI1bDQuODc1IDIuODEzbC0xLjY4NyAxbC00LTIuMzEzYTMuNyAzLjcgMCAwIDEtMS43NS0yLjI1Yy0uMjUtLjkzNy0uMTg4LTIuMDYyLjMxMi0yLjkzN00xNy43NSAxMS43NWwtNC44NzUtMi44MTJsMS42ODctMWw0IDIuMzEyYy42MjUuMzc1IDEuMTI1Ljg3NSAxLjQzOCAxLjVzLjUgMS4zMTMuNDM3IDIuMDYzYTMuNyAzLjcgMCAwIDEtLjc1IDEuOTM3Yy0uNDM3LjU2My0xIDEtMS42ODcgMS4yNXYtNC43NWMwLS4xMjUgMC0uMjUtLjA2My0uMzEyYzAgMC0uMDYyLS4xMjYtLjE4Ny0uMTg4bTEuNjg3LTIuNXMtLjA2Mi0uMDYyLS4xMjUtLjA2MmwtNC0yLjMxM2MtLjEyNS0uMDYyLS4xODctLjA2Mi0uMzEyLS4wNjJzLS4yNSAwLS4zMTMuMDYyTDkuODEyIDkuNjg4VjcuNzVsNC4wNjMtMi4zNzVjLjYyNS0uMzc1IDEuMzEyLS41IDIuMDYyLS41Yy42ODggMCAxLjM3NS4yNSAyIC42ODhjLjU2My40MzcgMS4wNjMgMSAxLjMxMyAxLjYyNXMuMzEyIDEuMzc1LjE4NyAyLjA2Mm0tMTAuNSAzLjVsLTEuNjg3LTFWNy4wNjNjMC0uNjg4LjE4Ny0xLjQzOC41NjItMkM4LjE4NyA0LjQzOCA4Ljc1IDQgOS4zNzUgMy42ODhhMy4zNyAzLjM3IDAgMCAxIDIuMDYyLS4zMTNjLjY4OC4wNjMgMS4zNzUuMzc1IDEuOTM4LjgxM2MwIDAtLjA2My4wNjItLjEyNS4wNjJsLTQgMi4zMTNhLjUuNSAwIDAgMC0uMjUuMjVjLS4wNjMuMTI1LS4wNjMuMTg3LS4wNjMuMzEyem0uODc1LTJMMTIgOS41bDIuMTg3IDEuMjV2Mi41TDEyIDE0LjVsLTIuMTg4LTEuMjV6Ii8%2BPC9zdmc%2B&logoColor=white" alt="Add to ChatGPT"></a>
      <br><sub>Plugins → <b>+</b> → Add custom MCP server,<br>then paste the address.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://cursor.com/en/install-mcp?name=whiteboard-animation&config=eyJ1cmwiOiJodHRwczovL21jcC53aGl0ZWJvYXJkYW5pbWF0aW9uLmFpL21jcCJ9"><img src="https://img.shields.io/badge/Add%20to%20Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white" alt="Add to Cursor"></a>
      <br><sub>Installs into Cursor;<br>sign in from Settings → MCP.</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://vscode.dev/redirect/mcp/install?name=whiteboard-animation&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmcp.whiteboardanimation.ai%2Fmcp%22%7D"><img src="https://img.shields.io/badge/Add%20to%20VS%20Code-0098FF?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0iI2ZmZmZmZiI%2BPHBhdGggZD0iTTE1LjQzNCAxLjcyOUwxMi4xNC4xNDVhMSAxIDAgMCAwLS40MzEtLjA5OGMtLjM1NiAwLS41MjkuMTY1LS41NTQuMTgyYS43LjcgMCAwIDAtLjE1MS4xMWwtNi4zMDYgNS43NWwtMi43NDctMi4wODRhLjY2NC42NjQgMCAwIDAtLjg1MS4wMzhsLS44ODEuOGEuNjY1LjY2NSAwIDAgMC0uMDAxLjk4NkwyLjYgOEwuMjE3IDEwLjE3YS42NjUuNjY1IDAgMCAwIC4wMDEuOTg1bC44ODEuODAyYS42NjUuNjY1IDAgMCAwIC44NTEuMDM4bDIuNzQ3LTIuMDg0bDYuMzA2IDUuNzVzLjA2OS4wNjguMTUyLjExYy4wMjQuMDE3LjE5OC4xOC41NTQuMThhMSAxIDAgMCAwIC40MzItLjA5N2wzLjI5NC0xLjU4NGExIDEgMCAwIDAgLjU2Ni0uOTAxVjIuNjI5YTEgMSAwIDAgMC0uNTY2LS45MDF6bS04LjIxNyA2LjI3bDQuNzg1LTMuNjN2Ny4yNnoiLz48L3N2Zz4%3D&logoColor=white" alt="Add to VS Code"></a>
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

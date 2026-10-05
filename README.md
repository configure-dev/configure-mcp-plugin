# Configure Memory for Cursor

Bring your project context into Cursor.

Configure gives Cursor the project decisions, preferences, and goals you have already saved. Start a build with its requirements in hand, follow your existing writing preferences, or pick up a project without explaining the background again.

Your Configure profile can hold context you chose to keep while working with other AI tools. This plugin searches that profile and brings relevant details into your current task.

## Try it

- "Use my saved Configure project context to plan the onboarding flow."
- "Check Configure for my writing preferences before drafting this page."
- "What decisions did I save about this project's launch?"
- "Remember in Configure that this project's first release is web only."

The included skill searches for context relevant to the task and saves facts when you ask.

## Connect

You need a Configure account with saved context. Complete Configure sign-in when Cursor prompts you and review the requested access.

This repository uses the Agent Plugins format supported by Cursor: `plugin.json`, `mcp.json`, and `skills/`. See the [Cursor plugin documentation](https://cursor.com/docs/reference/plugins) for installation options.

You can also add the server directly through Cursor's MCP settings:

```json
{
  "mcpServers": {
    "configure": {
      "url": "https://mcp.configure.dev/"
    }
  }
}
```

A direct MCP connection adds the tools. The full plugin also includes the context skill.

## What is included

- A connection to Configure's general MCP server at `https://mcp.configure.dev/`.
- A skill for finding relevant saved context and handling explicit save requests.
- Plugin metadata for Cursor.

The package contains metadata and instructions. It has no backend source, credentials, executable scripts, or background hooks.

## Your data

Configure returns context from the account you connect. Cursor sends tool arguments to Configure and receives the results. Saving sends the facts in your request to your Configure profile. Access is limited to the context available in that account; installing this plugin does not grant access to another assistant's private conversation history.

The general server may also expose tools for apps you have linked separately. Those connections have their own permissions and are optional. The skill uses them only when relevant to your request. An empty memory search does not trigger a search of your email or calendar.

Review Cursor's tool confirmations and Configure's sign-in permissions. Keep API keys, passwords, and other secrets out of memory requests. Manage your saved context and connections in Configure.

## License

The files in this plugin package are available under the [MIT License](LICENSE). This license covers this wrapper only. Configure's hosted service, backend, and user data are outside its scope and remain subject to their applicable terms.

[Configure](https://configure.dev) | [Documentation and support](https://docs.configure.dev) | [Privacy](https://configure.dev/privacy.html) | [Terms](https://configure.dev/terms.html)

# Highly duplicated issue on claude.ai couldn't access to private repository<br>

* [Example 1 : Claude Code web interface doesn't see my private repos, while it sees private repos of one of my organizations.](https://github.com/anthropics/claude-code/issues/96670) <br>
* [Example 2 : Hi there. There is an issue as with claude AI I cant find any repo](https://github.com/anthropics/claude-code/issues/98250) <br>
* [Example 3 : I connected GitHub to claude.ai (Settings > Connectors > GitHub) so Claude could list my repositories and push code. My account has 8 private repositories and 0 public ones.](https://github.com/anthropics/claude-code/issues/98050) <br>

For affected organisations and individual searching for fixing guidance, the following guide will help you.<br><hr>
TLDR : Use OAuth Apps<br>
---
Starting from claude.ai<br>
1. Claude → Settings → Connectors
- a. Remove the Github connectors you discover
- b. Add custom connector
- c. Name: Github
- d. Remote MCP server URL: https://api.githubcopilot.com/mcp 
- e. Hang on there
<br>

Moving to github<br>
<br>
2. GitHub → Settings → Developer settings → OAuth Apps → New OAuth App
- a. Name: Claude
- b. Homepage URL: https://claude.ai/
- c. Redirect URI: https://claude.ai/api/mcp/
- d. Enable Device Flow: no tick by default
- e. Click Register application
- f. Generate a new client secret

<br>
Back to claude.ai<br>
<br>

3. Copy Client ID & client secret into Claude.ai custom connector
4. Connect
5. Authorize 

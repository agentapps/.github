<div align="center">

<h1>Agent Apps</h1>

<p><strong>Connect everything. Stay in control.</strong></p>

<p>Applications built for AI agents, and the rules that decide what each agent may do with them.</p>

[![npm](https://img.shields.io/npm/v/@agentapps/cli?label=%40agentapps%2Fcli&color=ffbb0a)](https://www.npmjs.com/package/@agentapps/cli)
[![CI](https://github.com/agentapps/agentapps/actions/workflows/ci.yml/badge.svg)](https://github.com/agentapps/agentapps/actions/workflows/ci.yml)
[![Node](https://img.shields.io/badge/node-24%20%7C%2026-brightgreen)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/agentapps/agentapps/blob/main/LICENSE)

</div>

---

An **Agent App** gives an agent tools to act, UI to show what it did, events to tell it what happened and hooks to take part in the conversation. The platform keeps what an app should not own: credentials, storage, permissions and the policy that says which agent may call which tool.

It is an open protocol. Any agent platform that speaks MCP can use Agent Apps through a gateway: Claude Code, Codex, Cursor, Gemini CLI, VS Code, Windsurf, Zed.

### Install

```bash
npm install -g @agentapps/cli
```

```bash
agentapps install app.github github-work    # an app, under a name you choose
agentapps github-work auth                   # your account, kept on your machine
agentapps station start                      # runs your apps
agentapps connect claude-code                # or: agentapps connect cursor
```

### You decide what each agent may do

Every connected agent has its own key and its own policy. A rule allows a tool, denies it, or makes the call wait for your approval:

```bash
agentapps policy set cursor app.github merge-pull ask
agentapps policy set claude-code app.github git-push deny
```

### A catalog of apps

GitHub, Notion, Slack, Gmail, Google Calendar and Drive, Linear, Jira, Stripe, HubSpot, Figma, Sentry, Vercel, Supabase and many more. `agentapps apps` lists them, and each one installs with a single command. The whole catalog is at [agentapps.tech/catalogue](https://agentapps.tech/en/catalogue).

### Write your own

```bash
npm create @agentapps <app-id>
```

The scaffolder brings the test harness and a skill that walks a coding agent through research, tool design, tests and a live check.

---

<div align="center">

[**Website**](https://agentapps.tech) · [**Repository**](https://github.com/agentapps/agentapps) · [**Docs**](https://docs.agentapps.tech) · [**Contributing**](https://github.com/agentapps/agentapps/blob/main/CONTRIBUTING.md)

<sub>Maintained by <a href="https://github.com/supertowers">Pablo López Torres</a></sub>

</div>

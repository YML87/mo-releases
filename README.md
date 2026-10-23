<p align="center">
  <img src="docs/images/mo-hero.png" alt="Meet Mo. Your work companion. Your connection to monō." width="100%">
</p>

<p align="center">
  <img src="docs/images/mo-icon.png" alt="Mo app icon" width="96">
</p>

<h2 align="center">Install Mo with your AI agent</h2>

<p align="center">
  Copy the prompt in <a href="#install-with-your-agent"><b>Install with your agent</b></a> into Claude Code, T3 or a similar agent.<br>
  <sub>APPLE SILICON (M1 OR LATER) · FOR MONŌ INTERNAL TESTERS · INSTALLERS ONLY, NO SOURCE CODE</sub>
</p>

---

## What Mo is

Mo is an AI work companion for your Mac. It brings **voice dictation** and **conversation with monō** into one app, so you can speak instead of type, think your work through, and send approved requests to agents through **T3**.

- **Mo** is the companion you talk to.
- **monō** is the AI platform behind the conversation.
- **T3** runs the connected agent work and keeps its conversations.

<p align="center">
  <img src="docs/images/mo-states.png" alt="Mo listening, thinking, speaking and ready" width="100%">
</p>

## Install with your agent

**This is the only supported way to install Mo for now.** Downloading the installer in a browser triggers a macOS security warning, because Mo isn't Apple-notarised yet. Paste this prompt into your AI coding agent (Claude Code, T3 or similar). It downloads Mo with a Terminal command, checks the file's fingerprint and puts Mo in Applications.

```text
Install (or update) the Mo desktop app for me from https://github.com/YML87/mo-releases.

1. Get the latest release tag from
   https://api.github.com/repos/YML87/mo-releases/releases/latest
   (call the version without the "v" VERSION).
2. In a new empty folder, use curl to download mo-VERSION-arm64.dmg and
   mo-release-receipt.json from
   https://github.com/YML87/mo-releases/releases/download/<tag>/
3. Check the DMG's SHA-256 matches sha256["mo-VERSION-arm64.dmg"] in the receipt.
   If it doesn't match, stop and tell me. Don't install anything.
4. Quit Mo if it is running. If /Applications/mo.app exists, move it to the Trash.
5. Clear Mo's old macOS permission records, so the new version can be allowed fresh:
   for s in Accessibility Microphone AppleEvents ScreenCapture AudioCapture; do
     tccutil reset "$s" co.monoai.mo; done
6. Mount the DMG read-only (hdiutil attach -nobrowse -readonly), copy mo.app into
   /Applications with ditto, then detach the DMG and delete the download folder.
7. Confirm with: codesign --verify --deep --strict /Applications/mo.app
8. Don't open Mo yourself. Open the Accessibility settings for me with:
   open "x-apple.systempreferences:com.apple.preference.security?Privacy_Accessibility"
   Then tell me, step by step:
   a. Open Mo from Applications myself (in Finder or Spotlight).
   b. Allow the Microphone when Mo asks.
   c. In Accessibility, switch mo on. If it isn't listed, click +, choose
      /Applications/mo.app, and switch it on.
   d. Quit Mo (Cmd+Q) and open it again, then try dictating.
   e. If Mo asks to control System Events, choose Allow.
```

**Then follow your agent's steps.** In short: open Mo yourself, allow the Microphone, switch mo on under **System Settings → Privacy & Security → Accessibility**, then **quit Mo and open it again** before dictating.

**Dictation copies but doesn't paste?** Remove mo from the Accessibility list (select it, click −), add it again with +, switch it on, then quit and reopen Mo. After an update, the old entry can look switched on but no longer work.

**To update Mo,** paste the same prompt again. You'll need to allow Microphone and Accessibility again after each update, until Mo is signed with an Apple Developer ID.

> This skips Apple's check rather than passing it. The fingerprint check still refuses a broken or swapped download. Use it only for Mo from this page.

## What works today

| Feature | What it does |
|---|---|
| 🎙️ **Voice dictation** | Speak and your words appear as text in the app you're using. |
| 💬 **Chat with monō** | Ask questions, develop ideas and think your work through. Dictation and chat are separate today, not one spoken conversation. |
| 🧠 **Saved context** | Chats, summaries and your confirmed decisions are saved to Mo Brain. Choose **Don't save this chat** to turn that off. |
| 📁 **Project context** | The chat header shows the current project, open jobs and latest checkpoint from Mo Brain. These are saved records, not a live check. |
| 🔗 **Work through T3** | Authorise Mo in your browser, pick a project and conversation, and review every message or agent request before it's sent. |
| ⬆️ **Update check** | **Settings → System → Check for updates** tells you when a new version is out. Install it by pasting the agent prompt again. |

<details>
<summary><b>How the T3 connection works</b></summary>

<br>

Mo remembers approved T3 access and connects automatically while both apps are running. Expired or revoked access needs authorising again. Connection problems may need attention; permanent availability is not promised.

Normal Mo chat never starts agents or sends work on its own. Agent requests go to an existing monō conversation in T3 for coordination, and a queued request is not proof an agent has started.

Mo records its integration requests, receipts and failures, and shows the activity T3 reports, not every action on your computer. T3 keeps its own conversations even when **Don't save** is on.

</details>

## Coming soon

| Feature | Status |
|---|---|
| **Chat-to-work handoff.** Ask, prepare a request, approve it once and track the result | Built and tested, not live yet |
| **Start new work from Mo.** New T3 conversation or project, or open Terminal in a project folder | Built and tested, not live yet |
| **Calendar connections.** Google Calendar and Microsoft calendars | Waiting on monō sign-in keys |
| **Automatic project discovery.** Find and open the right project when the match is clear | Proposed |
| **Company data access.** Find permitted information through monō's company connections | Needs wiring and testing |
| **Screen awareness.** Help in context, with your permission | Not yet a working capability |
| **Spoken conversation and computer actions.** Talk with Mo and let it carry out approved tasks | Not yet a working capability |


---

<p align="center"><sub>MO · BY MONŌ AI · SYDNEY</sub></p>

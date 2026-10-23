# Meet Mo

**Your work companion. Your connection to monō.**

Mo is an AI work companion for your Mac. Mo Desktop brings voice dictation and conversation with monō into one app.

Its purpose is to reduce the effort of using your computer. Speak instead of typing. Think through work with Mo. Send approved requests to agents through T3.

Mo is the companion you interact with. monō provides the AI platform behind the conversation. T3 manages the connected agent work and its conversations.

> **This page is for monō internal testers.** It holds Mo's downloadable installers only. There is no source code here.

## Download and install

1. Open the **[Releases](../../releases)** page and choose the newest Mo version.
2. Download **mo-VERSION-arm64.dmg**. This is the installer: a disk image that opens like a small window.
3. Open it and drag **Mo** onto the **Applications** folder.
4. Open Mo from Applications. This build is not yet Apple-notarised, so macOS may stop the first open. Go to **System Settings → Privacy & Security**, find the message about Mo and choose **Open Anyway**.
5. When asked, allow Mo the permissions it needs (microphone, and Accessibility for pasting dictated text).

**Needs:** a Mac with Apple Silicon (M1 or later). Intel Macs are not supported.

**What the other files are:**

- **mo-VERSION-arm64.zip**: the same app in a zip, used by Mo's own update check. You do not need it.
- **latest-mac.yml** and **mo-release-receipt.json**: the checklist of file sizes and fingerprints Mo uses to confirm a download is genuine. You do not need them.

## What works today

- **Voice dictation.** Speak and turn your words into text in the app you are using. Mo appears in the dictation control.
- **Text conversation with monō.** Use Mo’s chat to ask questions, develop ideas and think through your work. Dictation and AI chat are separate flows today, not a complete spoken conversation.
- **Saved chat context.** Mo Desktop saves chats, summaries and your confirmed decisions to Mo Brain. The “Don’t save this chat” option turns off Mo’s chat saving.
- **Project context.** The chat header displays the current project, open jobs and latest checkpoint recorded in Mo Brain. These are saved records, not a live check of the project.
- **Approved work through T3.** Authorise Mo in your browser, then use its T3 panel to select a project and conversation. Review messages or agent requests before sending. Read replies, inspect reported activity and open the original conversation in T3.
- **Update check.** In **Settings → System**, choose **Check for updates**. Mo looks only at this page's releases, only when you click, and checks the download before opening it. You then install the new version by hand.

## How the connection works

Mo remembers approved T3 access and connects automatically while both apps are running. Expired or revoked access needs authorisation again. Connection problems may need attention; permanent availability is not promised.

The installed workflow uses explicit T3 controls. Normal Mo chat does not independently start agents or send work. Agent requests from standalone Mo go to an existing monō conversation in T3 for coordination. A queued request is not proof that an agent has started.

Mo records its integration requests, receipts and failures. It also displays the activity T3 reports, not every action on your computer. T3 keeps its own conversations even when Mo’s “Don’t save” option is on.

## Coming soon

*These capabilities are not part of the accepted live workflow. Some are built candidates; others are planned.*

- **Chat-to-work handoff.** Ask Mo, prepare a request, review it, approve it once and track the result. Built and tested; not installed or live-tested yet.
- **Start new work from Mo.** Open a new T3 conversation, create a new T3 project, or open Terminal in a project folder. Built and tested; not installed or live-tested yet. Terminal opens in the folder only; Mo does not type or run commands.
- **Calendar connections.** Connect Google Calendar and Microsoft calendars. Sign-in keys for monō are not set up yet, so these do not work today.
- **Automatic project discovery.** Find the relevant project and conversations, open them and report status without picker clicks when the match is clear. Proposed, not built.
- **Screen awareness.** Understand your on-screen activity with your permission and help in context. Not established as a working Mo capability.
- **Company data access.** Find permitted information through monō’s company connections. Those connections still need wiring and testing in Mo.
- **Spoken conversation and computer actions.** Talk with Mo and let it carry out approved tasks in your apps. Not established as a working Mo capability.

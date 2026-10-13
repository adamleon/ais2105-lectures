# Setting up a computer for editing with a live preview

You only need this for previewing lectures on your own computer while you write them. Quick
fixes work without any setup: press `.` on the repo's GitHub page.

## Once per computer

1. Install **Node.js 24** (the LTS version) from https://nodejs.org/en/download. Accept the
   defaults.
2. Install **Git** from https://git-scm.com. Accept the defaults. npm needs Git to download the
   Lysark engine.
3. Install **VS Code** from https://code.visualstudio.com if you don't have it.
4. In VS Code, press F1, run **Git: Clone**, paste
   `https://github.com/adamleon/ais2105-lectures.git`, and pick a folder. Open the folder when
   VS Code asks, and answer **Yes, I trust the authors**.
5. Open a terminal: **Terminal > New Terminal**. On Windows, check that it says **cmd** at the
   right of the terminal panel. If it says **powershell**, click the **∨** next to the **+**,
   pick **Command Prompt**, and use that one: on a new Windows PC, PowerShell refuses to run npm
   ("running scripts is disabled on this system").
6. In the terminal, run these three lines, with your own name and the email address on your
   GitHub account:

   ```
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   npm install
   ```

   The two `git` lines tell Git who you are; without them, committing fails. `npm install`
   downloads the Lysark engine into a `node_modules` folder; the first time it takes a minute.

## Each time you work

1. **Pull first.** Click the sync icon (↻) next to `main` at the bottom left of the window and
   answer **OK** (or press F1 and run **Git: Pull**). Fixes made in the browser editor or on
   another computer aren't on this computer until you do.
2. **Bring the engine up to date** in the terminal:

   ```
   npm install
   ```

   It takes a second when nothing has changed. If the engine version changed in what you pulled,
   this installs the new engine, so your preview matches the published lectures.
3. **Start the preview:**

   ```
   npm run dev
   ```

   Open the address it prints (usually http://localhost:5173). If the course has more than one
   lecture, pick one from the list; `npm run dev -- baneplanlegging` opens one directly. The
   preview updates every time you save `slides.md`. Stop it with Ctrl+C in the terminal.
4. **Commit and push** from the Source Control view when you're done. The first push on a
   computer opens a window asking you to sign in to GitHub; choose to sign in with your browser
   and approve it. The site updates about two minutes after the push.

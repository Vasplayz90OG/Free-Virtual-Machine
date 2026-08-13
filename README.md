# ⚡ Free-VMS | Ultimate Leapfrog Engine



Warning: This project abuses GitHub Actions to create free, ephemeral VPS environments. Use a burner GitHub account. I am not responsible if GitHub bans your main account for violating their ToS.

🧠 What is this?
This is the ultimate, bulletproof GitHub Actions VPS workflow. It features 5 redundant SSH links, automatic file
backups, and a 1-click command to spawn isolated external Docker VPS environments.

No credit cards. No dedicated servers. Just pure cloud infrastructure automation.

✨ Features

🔗 5 Redundant SSH Links: Generates 5 separate Tmate links per session. If one link crashes, lags, or disconnects, you just use the next one.
🔄 Auto-Backup: Automatically commits and pushes any files in the VPS to your GitHub repo every 30 minutes. You never lose your work when it leapfrogs.
🐳 1-Click External VPS: Includes a newvps.sh command inside the main VPS to instantly spawn a fresh, isolated Ubuntu Docker container with its own Tmate link.
⏳ Auto-Leapfrog: Automatically restarts the VPS every 6 hours to bypass GitHub's execution time limits.

🚀 Quick Start

1. Setup the Workflow

Fork or clone this repository, go to the Actions tab, select Ultimate Multi-Link VPS, and click Run Workflow.

2. Get Your 5 Links

Wait 30 seconds, open the running workflow logs, and expand the Setup Main VPS & Generate 5 Links step. You will see 5 SSH links:

Main VPS Link #1: ssh xxxxxxx@nyc1.tmate.ioMain VPS Link #2: ssh yyyyyyy@nyc1.tmate.io...
Copy Link #1 and paste it into your terminal/SSH client.

3. Spawn an Isolated External VPS (Optional)

Once you are inside the main VPS, you can create a brand new, isolated Docker VPS with a single command.
./newvps.sh

It will print out a brand new SSH link. Open a new terminal window, paste that link, and hit Enter. You are now inside a completely fresh, isolated Ubuntu environment

⚠️ Limitations - 

6-Hour Timeout: GitHub forcefully terminates Action runners after 6 hours. The cron job will auto-restart it, but your 5 SSH links will change. Just check the Actions logs again for the new links.
Docker Access: The runner has sudo privileges, meaning you can install Docker and spawn containers inside your VPS!
File Storage: When the runner restarts, files outside the repository folder are destroyed. Make sure to keep your important files in the repository folder so the Auto-Backup can save them.

📜 License - 

MIT License

Copyright (c) 2026  ArizNodes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

<!-- Glowing Header -->
<p align="center">
  <img src="https://i.imgur.com/dBaSKWF.gif" height="40" width="100%">
</p>

<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=25&duration=3000&color=FF0000&background=000000&center=true&vCenter=true&width=600&lines=🚀+BRIAN+PRO;🔥+WhatsApp+Bot;💻+By+Brian+kimutai" alt="Typing Animation">
</h1>
name: Open new issue
on: workflow_dispatch

jobs:
  open-issue:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      issues: write
    steps:
      - run: |
          gh issue --repo ${{ github.repository }} \
            create --title "Issue title" --body "Issue body"
        env:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          

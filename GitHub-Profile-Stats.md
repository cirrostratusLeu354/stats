## GitHub Profile Stats Setup

TakaTime comes with a report generator that works with GitHub Actions to update your Profile README automatically.

1. Prepare your Profile Repo

   Go to your GitHub Profile Repository (the one named username/username).

   Go to Settings > Secrets and variables > Actions.

   Add a New Repository Secret named MONGO_URI with your connection string.

   (Optional) Add `GIST_TOKEN` if you plan to use Gists (not required for direct README updates).

2. Add the Markers

- Add start and end markers to your README.md

```md
<!--takatime-start-->

<h2 align="center">TakaTime Weekly Report</h2>

<p align="center">
  <img src="./public/taka-time.png" width="100%" alt="Time Stats" /><br/>
  <img src="./public/taka-languages30.png" width="400" alt="Languages" />
  <img src="./public/taka-projects30.png" width="400" alt="Projects" /><br/>
  <img src="./public/taka-languages.png" width="400" alt="Languages" />
  <img src="./public/taka-projects.png" width="400" alt="Projects" /><br/>
  <img src="./public/taka-tech.png" width="100%" alt="Tech Stack" />
</p>

<p align="center"><em>Generated automatically by <a href="https://github.com/Rtarun3606k/TakaTime">TakaTime</a></em></p>

<!--takatime-end-->
```

3. Create the Workflow

Create a file in your repo at .github/workflows/update-stats.yml and paste this content:

```yml

name: Update TakaTime Stats

on:
  schedule:
    - cron: "0 0 * * *" # Runs every midnight UTC
  workflow_dispatch:      # Allows manual trigger

jobs:
  update-readme:
    runs-on: ubuntu-latest
    permissions:
      contents: write # Needed to download releases

    steps:
      - name: Download Taka-Report Binary
        env:
          GH_TOKEN: ${{ github.token }}
        run: |
          # Downloads the latest stable binary
          gh release download --repo Rtarun3606k/TakaTime --pattern "taka-report-linux-amd64" --output taka-report
          chmod +x taka-report

      - name: Generate Report & Update Profile
        env:
          MONGO_URI: ${{ secrets.MONGO_URI }}
          GIST_TOKEN: ${{ github.token }}
          TARGET_REPO: ${{ github.repository }}
        run: ./taka-report -days=7 
```

`Note:` This workflow downloads the taka-report tool and runs it against your database to generate stats.


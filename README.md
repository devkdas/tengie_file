# Tengine Downloader

This repository contains a GitHub Actions workflow that automatically downloads the latest stable version of the [Tengine web server](https://tengine.taobao.org/).

## Overview

The workflow is defined in `.github/workflows/download-tengine.yml` and performs the following actions:

- **Scheduled Execution:** Runs automatically every day at 00:00 UTC to check for new versions.
- **Manual Trigger:** Can also be triggered manually from the "Actions" tab in the GitHub repository.
- **Dynamic Version Check:** Scrapes the official Tengine download page to find the URL of the latest version.
- **Download and Rename:** Downloads the `.tar.gz` file and renames it to `tengine_latest.tar.gz`.
- **Commit to Repository:** If the downloaded file has changed (i.e., a new version was released), the workflow commits the new `tengine_latest.tar.gz` file to the root of this repository.

## How to Use

The workflow is fully automated. No manual steps are required. You can view the workflow runs in the "Actions" tab of this repository.

To trigger the workflow manually:
1. Go to the **Actions** tab.
2. Select the **Download Latest Tengine** workflow from the list.
3. Click the **Run workflow** button.

The latest downloaded Tengine artifact will always be available in the root of this repository as `tengine_latest.tar.gz`.

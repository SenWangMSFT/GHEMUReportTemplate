# 📊 GitHub Enterprise Report Generator

This script generates a professional Excel report summarizing GitHub organization activity, including user permissions, committers, inactive users, and stale repositories.

## ✅ Prerequisites

* [Python installed](https://github.com/settings/tokens)
* Admin account of the GitHub Enterprise 
* A classic GitHub Personal Access Token (PAT) with the following scopes:

  * `read:org`
  * `repo`
  * `read:enterprise`

## 🚀 Setup Instructions

Follow these steps to install dependencies and run the script:

1. **Clone or download this repository**

   ```bash
   cd your/project/GHEMUReportTemplate
   ```

2. **Create and activate a Python virtual environment**

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. **Install the required dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your environment variables**

   * Create a `.env` file in the project root (you can copy the example):

     ```bash
     cp .env.example .env
     ```
   * In the `.env` file, set your GitHub token:

     ```env
     GITHUB_TOKEN=ghp_your_token_here
     ```

5. **Edit your GitHub Enterprise slug**

   * In `report.py`, set your enterprise slug:

     ```python
     ENTERPRISE_SLUG = "your-enterprise-slug"
     ```

6. **Run the report**

   ```bash
   python report-api.py
   ```

## 📁 Output

An Excel file named `GitHub_Enterprise_Reports.xlsx` will be generated in the current directory. It includes:

* Summary sheet
* User permission levels and chart
* Committer stats and chart
* Inactive user reports (90d, 180d)
* Stale repo count by organization

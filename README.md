# 📊 GitHub Enterprise Report Generator

This script generates a professional Excel report summarizing GitHub organization activity, including:

* User permissions
* Committers
* Inactive users (90 and 180 days)
* Stale repositories (not pushed to in 6+ months)

## ✅ Prerequisites

* [Python 3.11+ installed](https://www.python.org/downloads/)
* Admin account on your GitHub Enterprise
* A classic GitHub Personal Access Token (PAT) with the following scopes:

  * `read:org`
  * `repo`
  * `read:enterprise`

> 💡 [Generate your PAT here](https://github.com/settings/tokens)

## 🚀 Setup Instructions

Choose the setup instructions that match your operating system:

---

### 🔧 Unix/macOS/Linux (Bash)

```bash
# 1. Navigate to the project directory
cd your/project/GHEMUReportTemplate

# 2. Create and activate a virtual environment
python3.11 -m venv .venv
source .venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Copy and update your environment config
cp .env.example .env
# Edit .env and set: GITHUB_TOKEN=ghp_your_token_here

# 5. Set your GitHub Enterprise slug in report.py
# e.g., ENTERPRISE_SLUG = "your-enterprise-slug"

# 6. Run the report
python report-api.py
```

---

### 🖥️ Windows (PowerShell)

```powershell
# 1. Navigate to the project directory
cd "C:\Path\To\Your\Project\GHEMUReportTemplate"

# 2. Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# 3. Install dependencies
pip install -r requirements.txt

# 4. Copy and update your environment config
Copy-Item .env.example .env
# Edit .env and set: GITHUB_TOKEN=ghp_your_token_here

# 5. Set your GitHub Enterprise slug in report.py
# e.g., ENTERPRISE_SLUG = "your-enterprise-slug"

# 6. Run the report
python report-api.py
```

---

## 📁 Output

An Excel file named `GitHub_Enterprise_Reports.xlsx` will be generated in the project directory. It includes:

* ✅ Summary sheet
* ✅ User permission levels with a stacked bar chart
* ✅ Committer stats with visual comparison
* ✅ Inactive user reports (90 and 180 days)
* ✅ Stale repository count per org

Markdown
# GHTUN-Action 🚀

A high-performance network utility designed to run an Xray-core server via GitHub Actions, utilizing ngrok for public access. This project is a workflow-based adaptation of the original `.devcontainer` implementation.

## 🛠 Features
- **Automated Setup**: Installs Xray-core v26.3.27 and ngrok automatically.
- **Dynamic Security**: Generates a fresh UUID for every session.
- **Secure Tunneling**: Uses ngrok to expose the local Xray port to the internet.
- **Auto-Config**: Prints a ready-to-use VLESS link in the action logs.

## 📁 Project Structure
```text
├── .github/
│   └── workflows/
│       └── ghtun.yml       # GitHub Actions workflow file
├── config.json             # Xray configuration template
└── README.md               # Documentation
🚀 Getting Started
1. Prerequisites
A GitHub account.

An ngrok Authtoken. You can get one for free at ngrok.com.

2. Setup GitHub Secrets
To keep your credentials safe, you must add your ngrok token as a secret:

Navigate to your repository Settings.

Go to Secrets and variables > Actions.

Click New repository secret.

Name: NGROK_AUTHTOKEN

Value: YOUR_NGROK_AUTHTOKEN_HERE

3. Running the Workflow
Click on the Actions tab in your repository.

Select GHTUN-Runner from the left sidebar.

Click the Run workflow dropdown and press the green button.

4. How to Connect
Wait for the workflow to start (usually takes ~30 seconds).

Open the running job and expand the Configure and Start section.

Look for the VLESS Link printed in the logs.

Copy and paste the link into your client (e.g., v2rayN, Shadowrocket, or sing-box).

⚠️ Important Notes
Lifetime: GitHub Actions jobs are limited to 6 hours per run.

Account Safety: Ensure your ngrok token is kept secret and not hardcoded in the YAML file.

Usage: This project is intended for educational purposes and testing network protocols.

📄 License
MIT License

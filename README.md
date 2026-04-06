# 🤖 n8n News Digest Workflow

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/ambrose-kutti/n8n-news-digest?style=for-the-badge)](https://github.com/ambrose-kutti/n8n-news-digest/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/ambrose-kutti/n8n-news-digest?style=for-the-badge)](https://github.com/ambrose-kutti/n8n-news-digest/network)
[![GitHub issues](https://img.shields.io/github/issues/ambrose-kutti/n8n-news-digest?style=for-the-badge)](https://github.com/ambrose-kutti/n8n-news-digest/issues)
[![GitHub license](https://img.shields.io/github/license/ambrose-kutti/n8n-news-digest?style=for-the-badge)](LICENSE) <!-- TODO: Add a LICENSE file if not present -->

**Automate your daily news digest delivery straight to your inbox using n8n, RSS, and Gmail.**

</div>

## 📖 Overview

This repository provides an automated workflow designed with **n8n** to deliver a daily news digest directly to your email inbox. It integrates news from various **RSS feeds** and compiles them into a personalized email sent via **Gmail**, ensuring you stay updated effortlessly without manual checking.

## ✨ Features

- ⏰ **Daily Automation**: Automatically fetches and sends news updates on a scheduled basis.
- 📰 **RSS Feed Aggregation**: Gathers news articles from multiple specified RSS feeds.
- 📧 **Gmail Integration**: Delivers the compiled news digest directly to your chosen Gmail address.
- ⚙️ **No-Code/Low-Code**: Easily deployable and configurable using the n8n visual workflow editor.
- 🛠️ **Customizable**: Simple to modify RSS sources, email recipients, and email content within n8n.

## 🖥️ Screenshots

<!-- TODO: Add a screenshot of the n8n workflow canvas for better visualization -->

## 🛠️ Tech Stack

**Automation Platform:**
![n8n](https://img.shields.io/badge/n8n-241D3B?style=for-the-badge&logo=n8n&logoColor=FF478E)

**Integrations:**
![RSS](https://img.shields.io/badge/RSS-F26522?style=for-the-badge&logo=rss&logoColor=white)
![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)

**Workflow Definition:**
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)

## 🚀 Quick Start

This section will guide you through setting up and running the n8n news digest workflow.

### Prerequisites
- A running instance of **n8n** (self-hosted or cloud-based). You can find installation guides [here](https://docs.n8n.io/installation/).
- A **Gmail account** for sending the news digest emails.
- Configured **Gmail credentials** within your n8n instance. If you haven't set them up, refer to the [n8n Gmail credentials documentation](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.gmail/).

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ambrose-kutti/n8n-news-digest.git
   cd n8n-news-digest
   ```

2. **Import the workflow into n8n**
   - Open your n8n instance in a web browser.
   - Click on the **"Workflows"** tab.
   - Click **"New"** or **"Add Workflow"** (usually a `+` button).
   - Select **"Import from JSON"** or **"Upload JSON file"**.
   - Browse and select the `news bot.json` file from the cloned repository.
   - The workflow will now appear in your n8n workspace.

3. **Configure workflow credentials and settings**
   - Open the imported `news bot.json` workflow in n8n.
   - Locate the **Gmail node** and ensure it's configured with your active Gmail credentials.
   - Review the **RSS Feed nodes** (if multiple are present) and verify the URLs are correct or update them to your preferred news sources.
   - Adjust the **recipient email address** in the Gmail node if it's not set to your desired inbox.

4. **Activate the workflow**
   - Toggle the workflow to **"Active"** in the top right corner of the n8n workflow editor.
   - The workflow is now scheduled to run daily (based on the default trigger configuration within the JSON). You can also trigger it manually by clicking "Execute Workflow" to test.

## 📁 Project Structure

```
n8n-news-digest/
└── news bot.json    # The n8n workflow definition file
```

## ⚙️ Configuration

The primary configuration for this project is managed within the n8n workflow itself.

### Environment Variables (within n8n)
- **Gmail Credentials**: Managed securely within n8n's "Credentials" section. The workflow will reference these.
- **RSS Feed URLs**: Defined directly within the "RSS Read" nodes. You can easily modify these URLs to include or remove news sources.
- **Recipient Email**: Configured in the "Send Email" (Gmail) node to specify where the news digest is sent.

### Customizing the Workflow
- You can add or remove RSS feed nodes to change the sources.
- Modify the "Set" or "Code" nodes to change how the news content is processed and formatted before emailing.
- Adjust the "Cron" trigger node to change the schedule (e.g., from daily to hourly, or a different time).

## 🚀 Deployment

Deployment of this workflow simply involves activating it within your n8n instance:

1. Ensure all credentials are set up.
2. Verify RSS feed URLs and recipient email.
3. Toggle the workflow to `Active` in the n8n UI.

Once active, n8n will handle the scheduling and execution of the workflow based on its internal trigger settings.

## 🤝 Contributing

We welcome contributions! If you have suggestions for improvements or new features for this n8n workflow, please feel free to:

1. **Fork the repository.**
2. **Make your changes** to the `news bot.json` file.
3. **Submit a pull request** with a clear description of your changes.



## 🙏 Acknowledgments

- The incredible **n8n team** for building such a powerful and flexible automation platform.
- **RSS providers** for making news content easily accessible.
- **Gmail** for reliable email services.

## 📞 Support & Contact

- 🐛 Issues: [GitHub Issues](https://github.com/ambrose-kutti/n8n-news-digest/issues)
- 📧 For questions or further assistance, you can contact the repository owner. <!-- TODO: Add a specific contact email if desired -->

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ by [Ambrose Kutti](https://github.com/ambrose-kutti)

</div>

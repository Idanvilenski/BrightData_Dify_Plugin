# Bright Data Web Scraper Plugin for Dify

A comprehensive web scraping and data extraction plugin powered by Bright Data's enterprise-grade infrastructure with intelligent auto-detection. Supports 20+ platforms including Amazon, LinkedIn, Instagram, YouTube, and more.

![Plugin Demo](https://github.com/idanvilenski/BrightData_Dify_Plugin/blob/main/demo.png)

## 🚀 Quick Start

### 1. Download the Plugin
Download the latest plugin package: [`brightdata_plugin.difypkg`](https://github.com/idanvilenski/BrightData_Dify_Plugin/releases/latest/download/brightdata_plugin.difypkg)

### 2. Install in Dify
1. Go to [Dify.ai](https://dify.ai) → **Plugins** → **Add Plugin**
2. Choose **Add from Local File**
3. Upload the `brightdata_plugin.difypkg` file

### 3. Setup Bright Data Account
1. Visit [Bright Data](https://brightdata.com/) and create an account
2. Navigate to your account settings to get your API key
3. Copy your API token for the next step

### 4. Create Your First Workflow
1. Go to **Dify Studio** → **Workflow**
2. Add one of the **Bright Data Web Scraper** tools:
   - **Structured Data Feeds** - Extract structured data from 20+ platforms
   - **Scrape As Markdown** - Convert any webpage to clean markdown
   - **Search Engine** - Get search results from Google, Bing, Yandex

3. Enter your Bright Data API key when prompted
4. Connect an **LLM node** to process and summarize the scraped data

## 📋 Available Tools

### 🔍 Structured Data Feeds
Extract structured data from popular platforms:
- **E-commerce**: Amazon, eBay, Walmart, Best Buy, Etsy, Zara
- **Social Media**: Instagram, Facebook, TikTok, YouTube, X (Twitter)
- **Professional**: LinkedIn profiles, companies, jobs
- **Business**: Crunchbase, ZoomInfo
- **Maps & Reviews**: Google Maps, booking sites
- **News**: Reuters and other news sources

### 📄 Scrape As Markdown
Convert any webpage into clean, readable markdown format perfect for:
- Content analysis
- Documentation extraction
- Article processing

### 🔎 Search Engine
Get search results from major search engines:
- Google
- Bing
- Yandex

## 💡 Example Workflow

![Workflow Example](https://github.com/idanvilenski/BrightData_Dify_Plugin/blob/main/workflow-example.png)

**Sample Use Case**: Extract Amazon product information and create a summary
1. **START** → Input: Product URL
2. **STRUCTURED DATA FEEDS** → Extract product details
3. **LLM** → Summarize into easy-to-read text
4. **END** → Output: Clean product summary

## 🛠️ Development

### Building from Source
```bash
# Clone the repository
git clone https://github.com/idanvilenski/BrightData_Dify_Plugin.git
cd BrightData_Dify_Plugin

# Package the plugin
dify plugin package ./brightdata_plugin

# Sign the plugin (optional)
dify signature sign brightdata_plugin.difypkg -p your_key_pair.private.pem
```

### Requirements
- Python 3.11+
- Dify Plugin SDK
- Bright Data API access

## 📦 Installation Options

### Option 1: Local Upload (Recommended)
Download and upload the `.difypkg` file directly

### Option 2: GitHub Integration
Install directly from GitHub repository URL in Dify

### Option 3: Dify Marketplace (Coming Soon)
The plugin will be available in the official Dify Marketplace

## 🔧 Configuration

### API Key Setup
1. Get your API key from [Bright Data Dashboard](https://brightdata.com/cp/setting/users)
2. The key should start with your zone credentials
3. Enter the key in any Bright Data tool configuration

### Supported Parameters
- **URL**: Target website URL
- **Search Query**: Search terms for search engines
- **Engine**: Choose search engine (Google/Bing/Yandex)
- **Response Format**: JSON, Markdown, or Raw data

## 🎯 Use Cases

- **E-commerce Monitoring**: Track product prices and availability
- **Lead Generation**: Extract business information from LinkedIn
- **Content Research**: Gather articles and news for analysis
- **Market Research**: Monitor competitor websites and social media
- **SEO Analysis**: Track search engine results and rankings

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Issues**: [GitHub Issues](https://github.com/idanvilenski/BrightData_Dify_Plugin/issues)
- **Bright Data Support**: [Bright Data Help Center](https://help.brightdata.com/)
- **Dify Documentation**: [Dify Docs](https://docs.dify.ai/)

## 🏷️ Tags

`web-scraping` `data-extraction` `automation` `api-integration` `dify` `bright-data`

---

**⭐ If this plugin helps you, please star the repository!**
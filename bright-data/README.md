

# Bright Data Plugin for Dify

A comprehensive web scraping and data extraction plugin powered by Bright Data's enterprise-grade infrastructure. This plugin provides advanced web scraping capabilities with anti-bot detection for the Dify platform.

## Features

- 🔍 **Search Engine Scraping**: Google, Bing, Yandex search results
- 📄 **Web Page Scraping**: Extract content as Markdown or HTML
- 🛒 **E-commerce Data**: Amazon, Walmart, eBay product information
- 👥 **Social Media**: LinkedIn, Instagram, TikTok, Facebook data
- 🏢 **Business Intelligence**: Company profiles, reviews, analytics
- 🗺️ **Local Data**: Google Maps reviews and business information

## Prerequisites

- Python 3.12 or higher
- Dify account (Cloud or Self-hosted)
- Bright Data API token

## Installation

### Option 1: Pre-built Package (Recommended)

1. **Download Plugin Package**
   - Go to [Releases](https://github.com/YOUR_USERNAME/bright-data-dify-plugin/releases)
   - Download the latest `bright-data.difypkg` file

2. **Install in Dify**
   - Log into your Dify dashboard
   - Go to **Plugins** → **Install from file**
   - Upload the `bright-data.difypkg` file
   - Click **Install**

3. **Configure API Token**
   - Click on the installed **Bright Data** plugin
   - Add your **Bright Data API Token** (get from [Bright Data Dashboard](https://brightdata.com/cp/zones))
   - Save configuration

4. **Start Using**
   - Create workflows and use Bright Data tools
   - No additional setup required!

### Option 2: Development/Debug Mode

Only use this if you want to modify the plugin or contribute to development:

1. **Clone Repository**
```bash
git clone https://github.com/YOUR_USERNAME/bright-data-dify-plugin.git
cd bright-data-dify-plugin
```

2. **Set Up Environment**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
pip install -r requirements.txt
```

3. **Configure Debug Connection**
```bash
cp .env.example .env
# Edit .env with your Dify debug credentials
```

4. **Run Development Server**
```bash
python -m main
```

### Getting Bright Data API Token

1. Sign up at [Bright Data](https://brightdata.com)
2. Go to your dashboard → **Zones**
3. Create a new zone or use existing one
4. Copy the **API Token**
5. Use this token when configuring the plugin in Dify

## Usage

### In Dify Workflows
1. Create a new **Workflow** or **Chatflow**
2. Add nodes and look for **Bright Data** tools:
   - **Search Engine**: Scrape Google/Bing/Yandex results
   - **Web Scraper (Markdown)**: Extract webpage content
   - **Amazon Product**: Get product details
   - More tools available...

### Example Workflow
```
START → Web Scraper (Markdown) → LLM → END
```

Input a URL, get scraped content, and have AI analyze it.

## Available Tools

| Tool | Description |
|------|-------------|
| Search Engine | Scrape search results from Google, Bing, Yandex |
| Web Scraper (Markdown) | Extract webpage content as Markdown |
| Web Scraper (HTML) | Extract webpage content as HTML |
| Amazon Product | Get Amazon product information |
| Amazon Product Reviews | Extract Amazon product reviews |
| Amazon Product Search | Search Amazon products |
| LinkedIn Profiles | Extract LinkedIn profile data |
| Instagram Profiles | Get Instagram profile information |
| Google Maps Reviews | Extract Google Maps business reviews |
| And many more... | 50+ specialized scraping tools |

## Troubleshooting

### Common Issues

**"handshake failed, invalid key"**
- Get a fresh debug key from Dify
- Update your `.env` file
- Restart the plugin

**"plugin already installed"**
- Uninstall the plugin from Dify first
- Restart the plugin script

**"no available node, plugin not found"**
- Make sure the plugin script is running
- Check that all tools are properly loaded

### Getting Debug Key
1. Dify Dashboard → Plugins → Debug section
2. Copy the debug key and remote URL
3. Update `.env` file
4. Restart plugin

## Development

To modify or extend this plugin:

1. **Add New Tools**: Create new files in `tools/` directory
2. **Update Provider**: Add new tools to `provider/bright-data.yaml`
3. **Test Locally**: Use `python -m main` for development
4. **Package**: Use Dify CLI to create `.difypkg` files

## Support

- **Issues**: [GitHub Issues](https://github.com/YOUR_USERNAME/bright-data-dify-plugin/issues)
- **Bright Data**: [Bright Data Support](https://brightdata.com/support)
- **Dify**: [Dify Documentation](https://docs.dify.ai)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

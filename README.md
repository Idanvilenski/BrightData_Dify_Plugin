# 🚀 Bright Data Plugin for Dify

A comprehensive web scraping and data extraction plugin powered by Bright Data's enterprise-grade infrastructure. This plugin provides advanced web scraping capabilities with anti-bot detection for the Dify platform.

## ✨ **New! Smart Data Extractor**

Our latest addition automatically determines the best extraction method for your needs:

- **🧠 Intelligent Auto-Detection**: Just describe what you want or provide any URL
- **🎯 20+ Data Sources**: Amazon, LinkedIn, Instagram, YouTube, TikTok, Crunchbase, and more!
- **⚡ One Tool for Everything**: No need to choose between multiple extractors

## 🔧 **Features**

### **Smart Data Extractor (Recommended)**
- **E-commerce**: Amazon products/reviews/search, Walmart, eBay, Best Buy
- **Social Media**: LinkedIn profiles/companies/jobs, Instagram, TikTok, Facebook, X/Twitter
- **Business Intelligence**: Crunchbase companies, Google Maps reviews, ZoomInfo
- **Content & Media**: YouTube videos/comments, Reddit posts, GitHub repositories
- **Real Estate**: Zillow property listings

### **Classic Tools** 
- **Web Page Scraping**: Extract content as Markdown or HTML with anti-bot protection
- **Search Engine Scraping**: Google, Bing, Yandex search results

## 🚀 **Quick Start**

### **Option 1: Download Pre-built Package (Easiest)**

1. **Download Plugin Package**
   - Go to [Releases](https://github.com/Idanvilenski/BrightData_Dify_Plugin/releases)
   - Download the latest `bright-data.difypkg` file

2. **Install in Dify**
   - Open your Dify dashboard
   - Go to **Plugins** → **Install from file**
   - Upload the `bright-data.difypkg` file
   - Click **Install**

3. **Configure API Token**
   - Click on the installed **Bright Data** plugin
   - Add your **Bright Data API Token** 
   - Save configuration

4. **Start Using!**
   - Create workflows and use the **Smart Data Extractor**
   - Or use individual tools like **Web Scraper** and **Search Engine**

### **Option 2: Development/Debug Mode**

Only use this if you want to modify the plugin:

1. **Clone Repository**
```bash
git clone https://github.com/Idanvilenski/BrightData_Dify_Plugin.git
cd BrightData_Dify_Plugin/bright-data
```

2. **Set Up Environment**
```bash
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

## 🔑 **Getting Bright Data API Token**

1. Sign up at [Bright Data](https://brightdata.com)
2. Go to your dashboard → **Zones**
3. Create a new zone or use existing one
4. Copy the **API Token**
5. Use this token when configuring the plugin in Dify

## 💡 **Usage Examples**

### **Smart Data Extractor Usage**

The Smart Data Extractor automatically detects what you want to extract:

#### **Example 1: Amazon Product Analysis**
```
Request: "Get Amazon product details including price and reviews"
URL: "https://amazon.com/dp/B08N5WRWNW"
→ Automatically uses Amazon extractor
```

#### **Example 2: LinkedIn Profile Research**
```
Request: "Extract LinkedIn professional profile information"
URL: "https://linkedin.com/in/elonmusk"
→ Automatically uses LinkedIn extractor
```

#### **Example 3: Instagram Analytics**
```
Request: "Get Instagram profile statistics and engagement"
URL: "https://instagram.com/instagram"
→ Automatically uses Instagram extractor
```

#### **Example 4: Business Intelligence**
```
Request: "Find company funding and investment data"
URL: "https://crunchbase.com/organization/openai"
→ Automatically uses Crunchbase extractor
```

### **Workflow Integration**

1. **Create a new Workflow** in Dify
2. **Add Smart Data Extractor node**
3. **Configure parameters**:
   - **Request**: Describe what you want
   - **URL**: Paste any supported URL
   - **Additional Parameters**: Leave empty (optional)
4. **Connect to LLM node** to process the extracted data
5. **Run and enjoy!**

## 🎯 **Supported Platforms**

| Category | Platforms |
|----------|-----------|
| **E-commerce** | Amazon, Walmart, eBay, Best Buy, Home Depot, Zara, Etsy |
| **Social Media** | LinkedIn, Instagram, TikTok, Facebook, X/Twitter, YouTube, Reddit |
| **Business Intel** | Crunchbase, ZoomInfo, Google Maps, Yahoo Finance |
| **Content & Apps** | GitHub, Reuters News, Google Play, Apple App Store |
| **Real Estate** | Zillow, Google Shopping |

## 🔧 **Configuration Parameters**

### **Smart Data Extractor**
- **Request** (required): Describe what data you want to extract
- **URL** (optional): Specific URL to extract from
- **Additional Parameters** (optional): JSON with extra settings like `{"pages_to_search": "3", "num_of_reviews": "50"}`

### **Web Scraper**
- **URL** (required): Webpage to scrape
- **Output format**: Markdown or HTML

### **Search Engine**
- **Query** (required): Search terms
- **Engine**: Google (default), Bing, or Yandex

## 🚨 **Troubleshooting**

### **Common Issues**

**"Could not determine appropriate tool"**
- Be more specific in your request
- Use full URLs with https://
- Try: "Get Amazon product info" instead of "get data"

**"API Error 400: Invalid input"**
- Check that URLs are complete and valid
- Ensure your BrightData API token is correct
- Verify you have sufficient credits

**Plugin not connecting**
- Restart the plugin: `Ctrl+C` then `python -m main`
- Check your `.env` file has correct debug credentials
- Refresh Dify and re-add the plugin

### **Debug Mode Issues**

**"Failed to connect to localhost:5003"**
- Make sure Dify is running with plugin daemon
- Get fresh debug credentials from Dify
- Update your `.env` file with new credentials

## 📊 **What's New in v0.1.0**

- ✅ **Smart Data Extractor**: Auto-detects best extraction method
- ✅ **20+ Data Sources**: Massive expansion from 3 to 20+ platforms
- ✅ **Intelligent URL Detection**: Automatically selects tools based on URLs
- ✅ **Natural Language Requests**: Describe what you want in plain English
- ✅ **Better Error Handling**: Helpful suggestions when things go wrong
- ✅ **Robust API Integration**: Handles various response formats gracefully

## 🤝 **Contributing**

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and test thoroughly
4. Commit: `git commit -m 'Add amazing feature'`
5. Push: `git push origin feature/amazing-feature`
6. Submit a pull request

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 **Support**

- **Issues**: [GitHub Issues](https://github.com/Idanvilenski/BrightData_Dify_Plugin/issues)
- **Bright Data Support**: [Bright Data Help Center](https://help.brightdata.com)
- **Dify Documentation**: [Dify Docs](https://docs.dify.ai)

## 🙏 **Credits**

- **Bright Data**: For providing the enterprise-grade web scraping infrastructure
- **Dify Team**: For creating an amazing AI workflow platform
- **Contributors**: Thank you to everyone who helps improve this plugin!

---


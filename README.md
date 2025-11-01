# 🔍 Developer Tools Research Agent

### **An intelligent AI-powered research agent that automatically discovers, analyzes, and recommends developer tools and technologies using web scraping and LLM analysis.**

----------

## 🚀 Features

-   🤖 **Autonomous AI Agent** built with LangGraph state machine
    
-   🌐 **Web Research** using Firecrawl for search and scraping
    
-   🧠 **LLM-Powered Analysis** with GPT-4o-mini for intelligent extraction
    
-   📊 **Structured Data Output** using Pydantic models
    
-   💡 **Smart Recommendations** tailored for developers
    
-   🔄 **Multi-Step Workflow** (Extract → Research → Analyze)
    

----------

## 🧱 Project Structure

```
developer-tools-research/
├── src/
│   ├── firecrawl.py       # Firecrawl API integration
│   ├── models.py          # Pydantic data models
│   ├── prompts.py         # LLM prompt templates
│   └── workflow.py        # LangGraph agent workflow
├── main.py                # CLI interface
├── .env                   # Environment variables
├── requirements.txt       # Python dependencies
└── README.md
```

----------

## ⚙️ Setup Instructions

### 1️⃣ **Clone the repository**

```bash
git clone https://github.com/yourusername/developer-tools-research.git
cd developer-tools-research
```

### 2️⃣ **Create a virtual environment and install dependencies**

```bash
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate

pip install -r requirements.txt
```

### 3️⃣ **Create a `.env` file**

```env
OPENAI_API_KEY=your_openai_api_key
FIRECRAWL_API_KEY=your_firecrawl_api_key
```

### 4️⃣ **Run the agent**

```bash
python main.py
```

----------

## 💬 Example Interaction

```
Developer Tools Research Agent

Developer Tools Query: best backend as a service platforms
```

**Agent Output:**

```
🔍 Finding articles about: best backend as a service platforms
Extracted tools: Supabase, Firebase, Appwrite, PocketBase, Nhost

🔬 Researching specific tools: Supabase, Firebase, Appwrite, PocketBase

📊 Results for: best backend as a service platforms
============================================================

1. 🏢 Supabase
   🌐 Website: https://supabase.com
   💰 Pricing: Freemium
   📖 Open Source: True
   🛠️  Tech Stack: PostgreSQL, JavaScript, TypeScript, React, Node.js
   💻 Language Support: JavaScript, Python, Dart, Swift, Kotlin
   🔌 API: ✅ Available
   🔗 Integrations: GitHub, Vercel, Netlify, AWS
   📝 Description: Open source Firebase alternative with PostgreSQL database

2. 🏢 Firebase
   🌐 Website: https://firebase.google.com
   💰 Pricing: Freemium
   📖 Open Source: False
   🛠️  Tech Stack: NoSQL, JavaScript, Cloud Functions
   💻 Language Support: JavaScript, Swift, Kotlin, Java, C++
   🔌 API: ✅ Available
   🔗 Integrations: Google Cloud, Analytics, BigQuery
   📝 Description: Google's comprehensive app development platform

3. 🏢 Appwrite
   🌐 Website: https://appwrite.io
   💰 Pricing: Free
   📖 Open Source: True
   🛠️  Tech Stack: Docker, PHP, MySQL, Redis
   💻 Language Support: JavaScript, Python, PHP, Ruby, Dart
   🔌 API: ✅ Available
   🔗 Integrations: Docker, GitHub, GitLab
   📝 Description: Self-hosted backend server for web and mobile developers

4. 🏢 PocketBase
   🌐 Website: https://pocketbase.io
   💰 Pricing: Free
   📖 Open Source: True
   🛠️  Tech Stack: Go, SQLite, JavaScript
   💻 Language Support: JavaScript, Go
   🔌 API: ✅ Available
   🔗 Integrations: Docker, Svelte, React, Vue
   📝 Description: Single-file backend with embedded SQLite database

Developer Recommendations:
----------------------------------------
For most projects, Supabase is the best choice because it's open-source, 
offers a generous free tier, and provides PostgreSQL's power with Firebase's 
ease-of-use. If you need a lightweight, self-hosted option, PocketBase is 
excellent at just 15MB with zero dependencies. Firebase remains best for 
projects deeply integrated with Google Cloud services, but expect higher 
costs at scale.
```

----------

### 📝 How It Works

The agent follows a **3-step workflow**:

1.  **🔍 Extract Tools** – Searches articles about your query and extracts specific tool names
    
2.  **🔬 Research** – Visits each tool's official website and scrapes detailed information
    
3.  **💡 Analyze** – Uses GPT-4 to generate intelligent recommendations based on findings
    

🛑 **To exit:** type `quit` or `exit`

----------

## 🧠 Technologies Used

-   🦜 **LangChain** – LLM application framework
    
-   🕸️ **LangGraph** – State machine for agent workflow
    
-   🌍 **Firecrawl** – Web search and scraping API
    
-   🤖 **OpenAI GPT-4** – Language model for analysis
    
-   📦 **Pydantic** – Data validation and structured outputs
    
-   🐍 **Python 3.8+** – Core programming language
    

----------

## 🎯 Use Cases

-   🔎 **Technology Discovery** – Find new tools and libraries
    
-   📊 **Competitive Analysis** – Compare similar developer tools
    
-   💰 **Pricing Research** – Understand cost structures
    
-   🛠️ **Tech Stack Decisions** – Make informed technology choices
    
-   📚 **Learning** – Discover what tools exist in any domain
    

----------

## 🔧 Configuration

### Customize Analysis

Edit `src/prompts.py` to modify:

-   Tool extraction criteria
-   Analysis focus areas
-   Recommendation style

### Adjust Workflow

Edit `src/workflow.py` to:

-   Change number of tools researched
-   Add conditional logic
-   Implement retry mechanisms

### Data Models

Edit `src/models.py` to:

-   Add custom fields
-   Modify data structures
-   Extend analysis capabilities

----------

## 📊 Data Models

### CompanyInfo
```python
{
    "name": str,
    "description": str,
    "website": str,
    "pricing_model": str,  # Free, Freemium, Paid, Enterprise
    "is_open_source": bool,
    "tech_stack": List[str],
    "api_available": bool,
    "language_support": List[str],
    "integration_capabilities": List[str]
}
```

----------


## 📄 License

This project is licensed under the MIT License.

----------

## 👨‍💻 Author

Developed with ❤️ for the developer community

🔗 [GitHub Repository](https://github.com/yourusername/developer-tools-research)

----------

## 🙏 Acknowledgments

-   **Firecrawl** for powerful web scraping capabilities
-   **LangChain** for the agent framework
-   **Anthropic** for inspiration from MCP protocol
-   **OpenAI** for GPT-4 API

----------


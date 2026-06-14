# 🛒 AI Shopping Assistant

![Python](https://img.shields.io/badge/Python-3.x-blue)
![LangChain](https://img.shields.io/badge/LangChain-Agent-green)
![Groq](https://img.shields.io/badge/LLM-Qwen3--32B-orange)
![Streamlit](https://img.shields.io/badge/UI-Streamlit-red)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey)
![Vision AI](https://img.shields.io/badge/Vision-Llama4--Scout-purple)
![Status](https://img.shields.io/badge/Status-Working-success)

An AI-powered Shopping Assistant built using LangChain Agents, Groq-hosted LLMs, SQLite, and Streamlit.

The assistant helps users discover products, compare ratings, apply filters, analyze uploaded product images, and place orders through natural language conversations.

This project demonstrates an end-to-end Agentic AI workflow where an LLM autonomously decides which tools to call, retrieves product information, evaluates ratings, and completes purchases.

---

# 🚀 Features

✅ AI-Powered Product Search

✅ LangChain Agent Tool Calling

✅ Product Recommendation System

✅ Customer Rating Analysis

✅ Organic Product Filtering

✅ Price-Based Filtering

✅ SQLite Product Catalog

✅ Natural Language Shopping

✅ Image-Based Product Search

✅ Vision AI Product Recognition

✅ Automated Order Placement

✅ Streamlit Chat Interface

✅ Multi-Step Agent Reasoning

✅ Structured Tool Architecture

---

# 📂 Project Structure

```text
shopping-assistant/
│
├── app.py
├── shopping_agent.py
├── review_api.py
│
├── resources/
│   ├── sample_images/
│   └── uploaded_products/
│
├── store.db
│
├── notebook.ipynb
│
├── .env.example
├── pyproject.toml
├── uv.lock
└── README.md
```

---

# 🏗 Architecture

```text
Customer
    │
    ▼
 Streamlit Chat UI
    │
    ▼
 LangChain Agent
    │
    ├── search_products()
    │
    ├── get_rating()
    │
    ├── describe_product_image()
    │
    └── checkout()
    │
    ▼
 SQLite Database
    │
    ├── Products
    └── Orders
    │
    ▼
 Groq LLM Models
    │
    ├── Qwen3-32B
    └── Llama-4-Scout
```

The application follows an Agentic AI architecture:

* UI Layer → Streamlit
* Agent Layer → LangChain Agent
* Tool Layer → Custom Tool Functions
* Database Layer → SQLite
* LLM Layer → Groq Models
* Vision Layer → Llama 4 Scout

This architecture allows the assistant to autonomously choose tools, retrieve data, analyze products, and complete shopping workflows.

---

# 🧠 Available Tools

The agent can dynamically choose from four tools.

### Product Search Tool

Searches products using:

* Product name
* Category
* Description
* Maximum price
* Organic preferences

---

### Rating Tool

Retrieves:

* Average customer rating
* Review count

for any product.

---

### Image Analysis Tool

Uses Vision AI to:

* Identify product type
* Extract product attributes
* Detect organic labels
* Generate search queries

from uploaded images.

---

### Checkout Tool

Creates orders and stores them in the database.

Returns:

* Order ID
* Product Name
* Price

---

# ⚙️ How It Works

### Step 1

Customer submits a shopping request.

Example:

```text
I want organic honey under $20 with at least 4.5 rating.
```

---

### Step 2

The LangChain Agent analyzes the request.

---

### Step 3

The agent calls:

```text
search_products()
```

to find matching products.

---

### Step 4

The agent calls:

```text
get_rating()
```

for each candidate.

---

### Step 5

Products are ranked and filtered.

---

### Step 6

The assistant recommends the best options.

---

### Step 7

Customer confirms the purchase.

Example:

```text
Order number 2
```

---

### Step 8

The agent calls:

```text
checkout()
```

and creates the order.

---

# 📷 Image Shopping Workflow

The assistant also supports image-based product discovery.

Example:

Upload a product image.

---

### Vision Pipeline

```text
Uploaded Image
        │
        ▼
Llama 4 Scout
        │
        ▼
Product Attribute Extraction
        │
        ▼
Search Query Generation
        │
        ▼
Product Search Tool
        │
        ▼
Recommended Products
```

The assistant can identify:

* Product category
* Product type
* Organic labels
* Similar products

directly from images.

---

# 💬 Example Queries

```text
I want organic honey under $20.

Show me almonds with rating above 4.5.

Find olive oil under $15.

Recommend healthy organic snacks.

Order number 2.

Get me the first product.

Yes, place the order.
```

---

# 🔑 Environment Setup

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
```

---

# ⚙️ Installation

Clone repository:

```bash
git clone https://github.com/YOUR_USERNAME/shopping-assistant.git

cd shopping-assistant
```

Create virtual environment:

```bash
python -m venv .venv
```

Activate environment:

Mac/Linux:

```bash
source .venv/bin/activate
```

Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
uv sync
```

---

# 🌐 Running the Application

Start Streamlit:

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

The dashboard allows users to:

* Search products using natural language
* Compare product ratings
* Upload product images
* Discover similar products
* Place orders directly
* Maintain conversation history

---

# 📸 Screenshots

## Product Search

![Product Search](assets/product-search.png)

---

## Image-Based Search

![Image Search](assets/image-search.png)

---

## Product Recommendations

![Recommendations](assets/recommendations.png)

---

## Order Placement

![Order Placement](assets/order-placement.png)

---

# 🤖 Agent Workflow

```text
User Request
        │
        ▼
Intent Analysis
        │
        ▼
Tool Selection
        │
        ├── Search Products
        ├── Get Ratings
        ├── Analyze Image
        └── Checkout
        │
        ▼
Reasoning & Decision Making
        │
        ▼
Final Response
```

---

# 📦 Tech Stack

### Programming Language

* Python

### AI Framework

* LangChain

### LLM Providers

* Groq

### Models

* Qwen3-32B
* Llama 4 Scout

### Database

* SQLite

### Frontend

* Streamlit

### AI Capabilities

* Tool Calling
* Agentic AI
* Vision AI
* Multi-Step Reasoning

---

# 📦 Requirements

```text
streamlit

langchain
langchain-core
langchain-groq

python-dotenv

sqlite3

pillow
```

Install:

```bash
uv sync
```

---

# 🧪 Testing Performed

✔ Product Search

✔ Price Filtering

✔ Organic Filtering

✔ Rating Retrieval

✔ Product Recommendation

✔ Vision-Based Product Search

✔ Order Placement

✔ SQLite Integration

✔ LangChain Tool Calling

✔ Streamlit Interface

✔ Multi-Step Agent Reasoning

---

# 👨‍💻 Development Notes

This project was developed to demonstrate how Agentic AI systems can automate real-world shopping workflows.

Instead of relying on fixed application logic, the assistant dynamically decides which tools to call, how to retrieve product information, how to evaluate ratings, and when to execute purchases.

The project demonstrates practical applications of:

* LangChain Agents
* Tool Calling
* Vision AI
* Agentic Workflows
* LLM Integration
* SQLite Databases
* Streamlit Applications

---

# 📄 License

This project was developed for educational, portfolio, and internship evaluation purposes.

No real payment processing is performed.

# 🤖 Personal Assistant-MCP-n8n Workflow

Workflow built in **n8n** that creates a conversational AI agent capable of responding to chat messages and invoking external tools (Airtable, Gmail) through **MCP (Model Context Protocol)**.  

---

## 📌 Executive Summary
This workflow leverages **n8n** and **MCP** to build an AI-powered assistant that can:  
- Receive and process chat messages.  
- Use **OpenAI Chat Model** for reasoning.  
- Trigger MCP-exposed tools via SSE endpoints (e.g., Airtable, Gmail).  
- Generate draft emails and update records automatically.  

The workflow enables centralized automation of operations in a **natural interface**.  

---

## 🚀 Problem & Opportunity
- **Problem (SDR context):**  
  Sales Development Reps (SDRs) spend too much time researching leads, drafting repetitive outreach emails, and managing data manually.  

- **Opportunity:**  
  Automating research and initial outreach increases efficiency, prioritizes relevant leads, and improves response rates.  

---

## ⚙️ Project Structure
```
Mcp-n8n/
│── MCP_Client.json          # Main workflow with AI Agent
│── MCP_Server_Airtable.json # MCP server for Airtable integration
│── MCP_Server_Gmail.json    # MCP server for Gmail integration
│── README.md                # Documentation
```

---

## 🔧 Requirements
- n8n installed (self-hosted or cloud).  
- Airtable and Gmail accounts.  
- OpenAI API Key.  

---

## ▶️ How to Use
1. Import the `.json` workflows into your **n8n** instance.  
2. Configure the required credentials (see section below).  
3. Run the workflows:  
   - **MCP_Client.json** to handle chat requests.  
   - **MCP_Server_Airtable.json** and **MCP_Server_Gmail.json** for external tool integration.  

---

## 🔑 Credentials Required
This workflow requires the following credentials configured in your n8n instance:

- **OpenAI API Key** → set in the `OpenAI Chat Model` node.  
- **Airtable** → configure your Airtable API Key in n8n Credentials.  
- **Gmail** → configure Gmail OAuth2 credentials in n8n.  

⚠️ Important: Credentials are **not included** in the JSON files (only references are stored).  
Each user must set up their own credentials in n8n before running the workflow.  

---

## 📊 Example Use Case
**Input:**  
- A new chat message from a potential lead.  

**Process:**  
- The AI agent uses OpenAI to reason over the input.  
- If needed, it triggers Airtable or Gmail MCP endpoints.  

**Output:**  
- Draft email prepared in Gmail.  
- Lead registered/updated in Airtable.  

---

## 👨‍💻 Author
Francisco Moyano Escalera  
Specialist in Data, AI & Automation  
📧 frannmmm419@gmail.com  
🌐 GitHub: [franm419](https://github.com/franm419)  



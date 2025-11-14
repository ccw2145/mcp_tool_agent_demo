# MCP Tool-Calling Agent Demo (Databricks + MCP)

A collection of Databricks notebooks demonstrating how to build and deploy a **tool-calling agent** that interacts with **MCP servers** using Unity Catalog and the **OpenAI / LangGraph SDKs**.  
The repo walks through creating UC tools, wiring an MCP server, testing end-to-end behavior, and comparing agent implementations (LangGraph vs OpenAI).

---

## 📘 Notebooks

| Notebook | Description |
|-----------|--------------|
| [1_create_uc_tools.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/1_create_uc_tools.ipynb) | Create and register Unity Catalog–backed tools for the agent. |
| [2a_langgraph-mcp-tool-calling-agent.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/2a_langgraph-mcp-tool-calling-agent.ipynb) | Build an MCP-aware agent using **LangGraph** for multi-step reasoning and tool orchestration. |
| [2b_openai-mcp-tool-calling-agent.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/2b_openai-mcp-tool-calling-agent.ipynb) | Implement an MCP tool-calling agent using the **OpenAI Responses API** (non-streaming). |
| [2c_openai-mcp-tool-calling-agent-streaming-output.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/2c_openai-mcp-tool-calling-agent-streaming-output.ipynb) | Same as 2b, but with **streaming intermediate output** for real-time feedback. |
| [3_test_mcp_server_agent.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/3_test_mcp_server_agent.ipynb) | End-to-end test for MCP server + agent integration. |
| [responses-agent-openai.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/responses-agent-openai.ipynb) | Extra experiments using the OpenAI Responses API with MCP tools. |
| [simple_tool.py.ipynb](https://github.com/ccw2145/mcp_tool_agent_demo/blob/main/simple_tool.py.ipynb) | Minimal MCP tool example written directly in a notebook. |

---

## 🧠 Overview

This demo shows how to:
- Define and register **Unity Catalog tools** for MCP integration.  
- Implement **custom MCP tools** hosted on Databricks Apps.  
- Build agents using either **LangGraph** or **OpenAI Responses** APIs.  
- Stream intermediate reasoning steps and outputs.  
- Deploy MCP-enabled agents to **Databricks Model Serving**.

---

## ⚙️ Quickstart

1. **Clone the repository**
   ```bash
   git clone https://github.com/ccw2145/mcp_tool_agent_demo.git
   cd mcp_tool_agent_demo
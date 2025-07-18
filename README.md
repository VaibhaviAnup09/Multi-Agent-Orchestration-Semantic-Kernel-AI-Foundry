# Multi-Agent Orchestration using Semantic Kernel and Azure AI Foundry

This project was developed as part of **Module 9** of the Microsoft AI Skills Challenge: *Create agentic AI solutions with Azure AI Foundry*. It demonstrates how to coordinate multiple Azure AI Foundry agents using **Semantic Kernel(SK)**, custom plugins, and strategy patterns for effective multi-agent orchestration in a simulated DevOps scenario.

---

## What I Learned

• How to define and configure multiple **Azure AI Foundry Agents** with distinct responsibilities  
• How to use **Semantic Kernel’s AgentGroupChat** to orchestrate conversations across agents  
• How to implement a **sequential selection strategy** and a **termination strategy** for multi-agent logic  
• How to build and integrate **custom plugins** for real-world operations (DevOps + log processing)  
• How to manage multi-turn, stateful conversations using Azure AI Foundry and Semantic Kernel  
• How to securely manage project credentials and deployment endpoints via `.env`, and exclude them using `.gitignore`

---

## Project Highlights

• Created two **Azure AI Foundry agents** with distinct roles:
  - `INCIDENT_MANAGER`: reads uploaded log files and decides next steps  
  - `DEVOPS_ASSISTANT`: performs recovery or escalation actions using plugin tools

• Used **Azure AI Foundry’s Python SDK** to create and deploy agents, run chats, and manage files  

• Uploaded sample log files into the pipeline and processed them one-by-one using Semantic Kernel’s chat interface  

• Orchestrated the interaction between agents using `AgentGroupChat` from Semantic Kernel  

• Applied:
  - `SequentialSelectionStrategy`: determines which agent responds next  
  - `ApprovalTerminationStrategy`: ends the conversation when the issue is resolved  

• Developed two custom plugins:
  - `DevopsPlugin`: performs real actions like restarting services, rolling back transactions, redeploying resources, or increasing quota  
  - `LogFilePlugin`: reads and returns contents of uploaded log files to support decision making  

• Logs are dynamically updated with actions taken by DevOps using the plugin system  

• Code organized in `agent_chat.py`, with custom strategy classes for full control of agent behavior  

• Used a `.env` file to store the Azure AI Foundry **project endpoint** and **model deployment name**, and ensured it’s ignored by Git with `.gitignore`

---

## Significance

This module gave me practical insight into **orchestrating multiple Azure AI Foundry agents** for collaborative reasoning and problem-solving. I learned how to design agent workflows where each agent has a specialized role and cooperates with others to complete a task.

The experience of coordinating agents with **Semantic Kernel’s Group Chat**, while grounding decisions on **real log file content**, made the project feel like a real-world DevOps incident resolution system. I now understand how to design and build **modular, pluggable multi-agent solutions** on Azure using Foundry and SK.

It reinforced how orchestration is not just about chaining outputs — but about managing agent interaction, decision-making, and contextual memory.

---

## Screenshots

• (assets/chat-output.png) (log1.png/log2.png/log3.png/log4.png)

---

## Reference

• Microsoft Learn : https://learn.microsoft.com/en-gb/collections/50wkaqtq50egz3?ref=collection&listId=60yka7t2o8od52&sharingId=6A9F03F25E12DA9E&wt.mc_id=aiskillsfest_msftlearn_training_wwl_challenge_tech

---

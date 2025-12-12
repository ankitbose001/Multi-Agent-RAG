# Multi-Agent RAG System - Company Policy Assistant (Powered by AWS Bedrock)
This repository contains the implementation of a Multi-Agent Retrieval-Augmented Generation (RAG) system designed to answer complex company policy questions using AWS Bedrock Agents , Lambda Functions, Amazon OpenSearchService

## Use Case
An Agentic AI powered assistant that searches multiple policy documents, company wiki , document repositories and summarizes company policy-related queries like:
> “What is the company's remote work policy?”

## Multi-Agent Architecture
 ![image](https://github.ibm.com/sughosh4/MultiAgent_RAG/assets/495198/86dfc643-8368-4f86-80d6-c4e624647171)


### Orchestrated Agent Pipeline
“Here’s how the multi-agent architecture works. The Orchestrator Agent receives the user query. If the context isn’t strong enough from the vector database, it spins up an execution loop involving four sub-agents:

•	🧠 Planner Agent: Breaks the query into sub-tasks.

•	🔍 Research Agent: Searches external/internal sources.

•	📝 Summarizer Agent: Condenses findings.

•	✅ Critique Agent: Validates whether the goal is met.”

•	The AI Model used to power the Agents is Anthropic Claude 3.5 Sonnet

### Workflow 
The user submits a natural language question. The Orchestrator first checks our vector DB via OpenSearch. If context is low, it calls the Planner Agent, which defines the task to be performed. Then, the Research Agent searches Organization Wiki and returns snippets. Summarizer distills that into key points from the returned snippets. Critique then checks: ‘Did this answer meet the original goal(User Query)?’ If yes, the response is returned. If no, the execution loop is repeated until the agents find a refined answer.

### Sample Query & Output:
The Agentic Network finds answers in seconds from a vast repository of company documents. Whether you’re in HR, compliance, or IT Support, this assistant reduces time to search information, speeds up decisions, and improves employee experience.”

Sample Query1:
 ![image](https://github.ibm.com/sughosh4/MultiAgent_RAG/assets/495198/bd89c125-dcca-4247-a02c-2c6795c841a4)




Sample Query 2:
 ![image](https://github.ibm.com/sughosh4/MultiAgent_RAG/assets/495198/94d56ff9-cc40-43aa-aab0-1f2129cf12d8)



Sample Query 3:
![image](https://github.ibm.com/sughosh4/MultiAgent_RAG/assets/495198/76181bbb-560b-4da1-9488-5d2f65deb42c)

 

### Conclusion:
With AWS Bedrock, OpenSearch, and intelligent agents, we can scale smart search across large enterprises and bring about process efficiency .Below are some real world use cases

Real World Use Cases
--------------------
1. Enterprise Policy & Compliance Assistant
✅ Use Case: Internal employee-facing assistant that answers company policy questions (like HR, travel, security policies) with source-backed responses.
🏢 Who Uses This: Large corporations, banks, law firms, governments
💡 Business Value: Reduces internal HR helpdesk load, ensures compliance adherence, helps search information quickly

2. Application Knowledge Base Assistant (Internal Tool Support) 
✅ Use Case: An Application Knowledge Base Assistant helps IT teams Search internal software application knowledge base
🏢 Who Uses This: IT support teams, Business analysts, Developers working across APIs or automation
💡 Business Value: Saves time spent searching scattered documentation, Reduces internal tickets to IT support, Improves productivity, Standardizes process execution

3. Legal Contract Review & Risk Analysis
✅ Use Case: AI assistant for lawyers to upload or reference contracts and identify unclear clauses, risks, and missing legal protections.
⚖️ Who Uses This: Law firms, legal tech startups, procurement teams
💡 Business Value: Speeds up legal review, reduces human errors

4. Financial Investment Analyst Assistant
✅ Use Case: Speeds up financial/stock research, due diligence and analysis of companies or markets for portfolio managers.
💹 Who Uses This: Hedge funds, fintech platforms, retail trading tools
💡 Business Value: Accelerates research, supports data-driven decisions

5. Healthcare Support System (for Doctors or Patients)
✅ Use Case: Helps Doctors and Medical professionals search through millions of medical documents / journals/records speeding up diagnosis.
🏥 Who Uses This: Hospitals, telemedicine providers, clinical researchers
💡 Business Value: Improves care quality, reduces time on routine queries and speeds up diagnosis






# product-agent-test
This is a lab test to create an agent that integrates with Foundry IQ to search and retrieve information from knowledge bases. It is creating a search resource, configure a knowledge base with sample data, build an agent in the portal, and then connect to it from Visual Studio Code to interact programmatically.

### Sample data: An outdoor company named Contoso is selling the outdoor & hiking facilities & items. The agent will ground the knowledge by leveraging the backpack guide, camping accessories & tent catalog - 3 PDF product files in total. 

## Steps:
### Step 1:
Create Foundry Project and Agent: Start a new project/hub, then build an agent with instructions to search knowledge bases exclusively for product queries.
​
### Step 2:
Set Up Foundry IQ: Provision Azure AI Search (Free/Basic tier), upload sample PDFs to Blob Storage (container: contosoproducts), and create a knowledge source (ks-contosoproducts) with embedding (text-embedding-3-small) and chat models (gpt).
​
### Step 3:
Test in Playground: Query the agent (e.g., "What types of tents does Contoso offer?") to verify retrieval, citations, and context awareness.

## Intro about the client App deployment
1.Clone this GitHub repo, configure .env with project endpoint/agent name, and complete agent_client.py using Microsoft Foundry SDK:

2.Connect via "AIProjectClient" and "DefaultAzureCredential".

3.Manage conversations with "openai_client.conversations.create/items.create/responses.create".

4.Handle MCP approval requests for knowledge base access (user prompts yes/no).

### Testing and Results
Run python agent_client.py and test queries like product categories, features, comparisons, and follow-ups. Observe approval flows, accuracy, citations, and context retention. Type "history" or "quit" to manage sessions

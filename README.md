# Microsoft Agent Framework In Action

A comprehensive hands-on guide to building intelligent agents using the Microsoft Agent Framework. This repository contains practical examples, tutorials, and code samples that demonstrate how to create powerful AI agents using both Python and .NET implementations.

## 🚀 What You'll Learn

This repository provides step-by-step tutorials and real-world examples covering:

- **Agent Foundations**: Core concepts and architecture of the Microsoft Agent Framework
- **Creating Your First Agent**: Build a simple travel planning agent from scratch
- **Framework Exploration**: Deep dive into different providers and configurations
- **Tools Integration**: Implement vision, code interpretation, and custom tools
- **Provider Patterns**: Work with MCP (Model Context Protocol) and Agent-to-Agent communication
- **RAG Implementation**: Build knowledge-enhanced agents with file search capabilities
- **Multi-Agent Systems**: Orchestrate multiple agents working together
- **Workflow Management**: Create complex agent workflows and pipelines

## 📁 Repository Structure

```
AgentframeworkInAction/
├── 01.AgentFoundation/           # Core concepts and architecture
├── 02.CreateYourFirstAgent/      # Getting started tutorials
│   └── code_samples/
│       ├── dotNET/              # C# implementation examples
│       └── python/              # Python implementation examples
├── 03.ExploerAgentFramework/    # Framework deep dive
│   └── code_samples/
│       ├── dotNET/              # .NET examples with various providers
│       └── python/              # Python examples with different configurations
├── 04.Tools/                    # Tool integration examples
│   └── code_samples/
│       ├── dotNET/              # Vision and code interpreter tools
│       ├── files/               # Sample assets
│       └── python/              # Python tool implementations
├── 05.Providers/                # Provider patterns and integrations
│   └── code_samples/
│       └── dotNET/
│           ├── 01-dotnet-agent-framework-aifoundry-mcp/
│           └── 02-dotnet-agent-framework-aifoundry-a2a/
├── 06.RAGs/                     # RAG implementation examples
│   └── code_samples/
│       ├── dotNET/              # .NET RAG implementations
│       ├── files/               # Knowledge base files
│       └── python/              # Python RAG examples
├── 07.MultiAgents/              # Multi-agent system examples
│   └── code_samples/
│       ├── dotNET/              # Sequential multi-agent workflows
│       └── files/               # Supporting assets
└── 08.Workflow/                 # Workflow management patterns
```

## 🛠 Prerequisites

***Note: This is internal priview intsallation guideline***

### Python Environment
- Python 3.10 or higher
- Install dependencies: 

```bash

pip uninstall agent-framework -y
pip uninstall agent-framework-azure -y
pip uninstall agent-framework-foundry -y

! pip install -r Installation\code_samples\python\requirements.txt --constraint Installation\code_samples\python\constraints.txt -U


```

### .NET Environment
- .NET 9.0 or higher
- Visual Studio 2022 or VS Code with C# extension


```bash

git clone https://github.com/microsoft/agent-framework.git

cd agent-framework

dotnet build agent-framework-dotnet.slnx


```

### Required Services
- Azure OpenAI Service and Azure AI Foundry
- GitHub Models (for some examples)
- Azure CLI (authenticated)
- Azure Developer CLI (authenticated)

## 🚀 Quick Start

### 1. Environment Setup

Create a `.env` file in the root directory with your configurations:

```env
# Azure OpenAI Configuration
AZURE_OPENAI_ENDPOINT=your_aoai_endpoint
AZURE_OPENAI_API_KEY=your_aoai_key
AZURE_OPENAI_DEPLOYMENT_NAME=your_model_deployment

# GitHub Models Configuration
GITHUB_TOKEN=your_github_token
GITHUB_ENDPOINT=https://models.inference.ai.azure.com
GITHUB_MODEL_ID=gpt-4o-mini

# Azure AI Foundry Configuration
FOUNDRY_PROJECT_ENDPOINT=your_foundry_endpoint
FOUNDRY_MODEL_DEPLOYMENT_NAME=your_model_name
```

### 2. Run Your First Agent (Python)

```python
from agent_framework.openai import OpenAIChatClient
from agent_framework import ChatAgent
from openai import AsyncOpenAI
import os

# Initialize client
client = AsyncOpenAI(
    api_key=os.environ.get("GITHUB_TOKEN"), 
    base_url=os.environ.get("GITHUB_ENDPOINT"),
)

# Create chat client
openai_chat_client = OpenAIChatClient(
    async_client=client, 
    ai_model_id=os.environ.get("GITHUB_MODEL_ID")
)

# Create agent
agent = ChatAgent(
    chat_client=openai_chat_client,
    instructions="You are a helpful AI assistant.",
)

# Run the agent
response = await agent.run("Hello, how can you help me?")
print(response.messages[-1].contents[0].text)
```

### 3. Run Your First Agent (.NET)

```csharp
using Azure.AI.Agents.Persistent;
using Azure.Identity;
using Microsoft.Extensions.AI.Agents;

var endpoint = Environment.GetEnvironmentVariable("FOUNDRY_PROJECT_ENDPOINT");
var modelId = Environment.GetEnvironmentVariable("FOUNDRY_MODEL_DEPLOYMENT_NAME");

var persistentAgentsClient = new PersistentAgentsClient(endpoint, new AzureCliCredential());

var agentMetadata = await persistentAgentsClient.Administration.CreateAgentAsync(
    model: modelId,
    name: "MyFirstAgent",
    instructions: "You are a helpful AI assistant."
);

AIAgent agent = await persistentAgentsClient.GetAIAgentAsync(agentMetadata.Value.Id);
AgentThread thread = agent.GetNewThread();

var response = await agent.RunAsync("Hello, how can you help me?", thread);
Console.WriteLine(response);
```

## 📚 Tutorial Progression

### Beginner Level
1. **01.AgentFoundation** - Understand the core concepts
2. **02.CreateYourFirstAgent** - Build a simple travel agent

### Intermediate Level
3. **03.ExploerAgentFramework** - Explore different providers (Azure OpenAI, GitHub Models, AI Foundry)
4. **04.Tools** - Add vision and code interpretation capabilities
5. **06.RAGs** - Implement knowledge-enhanced agents

### Advanced Level
6. **05.Providers** - Master MCP and Agent-to-Agent communication
7. **07.MultiAgents** - Build collaborative agent systems
8. **08.Workflow** - Create complex agent workflows

## 🔧 Key Features Demonstrated

- **Multiple Provider Support**: Azure OpenAI, GitHub Models, Azure AI Foundry
- **Tool Integration**: Vision analysis, code interpretation, custom functions
- **RAG Capabilities**: File search and knowledge base integration
- **Multi-Agent Orchestration**: Sequential and collaborative agent patterns
- **MCP Integration**: Model Context Protocol for enhanced capabilities
- **Streaming Responses**: Real-time agent interactions
- **Persistent Agents**: Stateful agent conversations

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔗 Resources

- [Microsoft Agent Framework Documentation](https://github.com/microsoft/agent-framework)
- [Azure AI Services](https://azure.microsoft.com/en-us/products/ai-services)
- [Azure AI Foundry](https://azure.microsoft.com/en-us/products/ai-foundry)
- [GitHub Models](https://github.com/marketplace/models)

## 🆘 Support

If you encounter any issues or have questions:
1. Check the individual README files in each chapter directory
2. Review the code samples for implementation details
3. Open an issue in this repository
4. Consult the official Microsoft Agent Framework documentation

---

**Start your journey with Microsoft Agent Framework today!** 🚀
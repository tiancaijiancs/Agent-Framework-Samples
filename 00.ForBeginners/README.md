# Microsoft Agent Framework for Beginners

Welcome to the comprehensive beginner's guide to the Microsoft Agent Framework! This directory contains hands-on tutorials, code samples, and practical examples designed to take you from zero to proficient in building AI agents using Microsoft's cutting-edge agent framework.

## 🎯 Learning Path Overview

This beginner's section is structured as a progressive learning journey, where each module builds upon the previous one:

```
00.ForBeginners/
├── 01-intro-to-ai-agents/          # 🚀 Start here: Your first AI agent
├── 02-explore-agentic-frameworks/  # 🔍 Understand agent architectures
├── 03-agentic-design-patterns/     # 🏗️ Learn design patterns
├── 04-tool-use/                    # 🛠️ Add tools to your agents
├── 05-agentic-rag/                 # 📚 Knowledge-enhanced agents
├── 07-planning-design/             # 🧠 Strategic planning agents
├── 08-multi-agent/                 # 🤝 Multi-agent collaboration
├── 09-metacognition/               # 🎭 Self-aware agents
├── 10-ai-agents-production/        # 🚀 Deploy to production
├── 11-agentic-protocols/           # 🔄 Communication protocols
└── 12-context-engineering/         # 📝 Context management
```

## 📚 Module Details

### 1. Introduction to AI Agents
**📁 Path:** `01-intro-to-ai-agents/`

Your journey begins here! Learn the fundamentals of AI agents and create your first travel planning agent.

**🔗 Code Samples:**
- [**Python Travel Agent**](01-intro-to-ai-agents/code_samples/python-agent-framework-travelagent.ipynb) - Build a vacation planning assistant
- [**C# Travel Agent**](01-intro-to-ai-agents/code_samples/dotnet-agent-framework-travelagent.ipynb) - .NET implementation

**🎯 What you'll learn:**
- Basic agent concepts and architecture
- Setting up your development environment
- Creating your first conversational agent
- Working with OpenAI and GitHub Models

### 2. Explore Agentic Frameworks
**📁 Path:** `02-explore-agentic-frameworks/`

Dive deeper into the Microsoft Agent Framework architecture and understand how agents think and operate.

**🔗 Code Samples:**
- [**Python Basic Agent**](02-explore-agentic-frameworks/code_samples/python-agent-framework-basicagent.ipynb) - Core framework concepts
- [**C# Basic Agent**](02-explore-agentic-frameworks/code_samples/dotnet-agent-framework-basicagent.ipynb) - .NET framework exploration

**🎯 What you'll learn:**
- Agent lifecycle and execution patterns
- Message handling and conversation flow
- Framework components and services
- Best practices for agent design

### 3. Agentic Design Patterns
**📁 Path:** `03-agentic-design-patterns/`

Master the fundamental design patterns that make agents effective and scalable.

**🎯 What you'll learn:**
- Common agent design patterns
- Separation of concerns in agent architecture
- Reusable agent components
- Scalability considerations

### 4. Tool Use
**📁 Path:** `04-tool-use/`

Transform your agents from conversational to functional by adding tool capabilities.

**🔗 Code Samples:**
- [**Python Tools Agent**](04-tool-use/code_samples/python-agent-framework-tools.ipynb) - Function calling and tool integration
- [**C# Tools Agent**](04-tool-use/code_samples/dotnet-agent-framework-tools.ipynb) - .NET tool implementation

**🎯 What you'll learn:**
- Function calling and tool integration
- Custom tool development
- Tool selection and orchestration
- Error handling in tool execution

### 5. Agentic RAG (Retrieval-Augmented Generation)
**📁 Path:** `05-agentic-rag/`

Build knowledge-enhanced agents that can access and reason over external information sources.

**🔗 Code Samples:**
- [**Python RAG Agent**](05-agentic-rag/python-agent-framework-aifoundry-file-search.ipynb) - Document search and retrieval
- [**C# RAG Agent**](05-agentic-rag/dotnet-agent-framework-aifoundry-file-search.ipynb) - .NET file search implementation

**🎯 What you'll learn:**
- File search and document retrieval
- Knowledge base integration
- Azure AI Foundry file search
- Information synthesis and reasoning

### 6. Planning and Design
**📁 Path:** `07-planning-design/`

Create agents that can break down complex tasks and create strategic plans.

**🔗 Code Samples:**
- [**Python Planning Agent**](07-planning-design/code_samples/python-agent-framrwork-ghmodel-planningdesign.ipynb) - Strategic task planning
- [**C# Planning Agent**](07-planning-design/code_samples/dotnet-agent-framrwork-ghmodel-planningdesign.ipynb) - .NET planning implementation

**🎯 What you'll learn:**
- Task decomposition and planning
- Strategic thinking in agents
- Complex workflow orchestration
- Decision-making frameworks

### 7. Multi-Agent Systems
**📁 Path:** `08-multi-agent/`

Learn how to create collaborative agent systems where multiple agents work together.

**🎯 What you'll learn:**
- Agent-to-agent communication
- Collaborative problem solving
- Distributed agent architectures
- Coordination and synchronization

### 8. Metacognition
**📁 Path:** `09-metacognition/`

Build self-aware agents that can reflect on their own thinking and improve their performance.

**🎯 What you'll learn:**
- Self-reflection in AI agents
- Performance monitoring and improvement
- Adaptive behavior patterns
- Learning from experience

### 9. Production Deployment
**📁 Path:** `10-ai-agents-production/`

Prepare your agents for real-world deployment with production-ready patterns and practices.

**🎯 What you'll learn:**
- Production deployment strategies
- Monitoring and observability
- Security and compliance
- Scaling considerations

### 10. Agentic Protocols
**📁 Path:** `11-agentic-protocols/`

Master advanced communication protocols for sophisticated agent interactions.

**🎯 What you'll learn:**
- Inter-agent communication protocols
- Message standards and formats
- Protocol design patterns
- Integration with external systems

### 11. Context Engineering
**📁 Path:** `12-context-engineering/`

Learn advanced techniques for managing context and memory in long-running conversations.

**🎯 What you'll learn:**
- Context window management
- Memory systems and persistence
- Conversation state management
- Context optimization techniques

## 🚀 Getting Started

### Prerequisites

**For Python Development:**
- Python 3.10 or higher
- pip package manager
- Virtual environment (recommended)

**For .NET Development:**
- .NET 9.0 or higher
- Visual Studio 2022 or VS Code with C# extension

**Required Services:**
- Azure OpenAI Service OR GitHub Models access
- Azure AI Foundry (for advanced examples)
- Azure CLI (authenticated)

### Quick Setup


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

## 🎯 Learning Objectives

By completing this beginner's series, you will:

- ✅ **Understand AI Agent Fundamentals** - Core concepts, architecture, and design principles
- ✅ **Build Production-Ready Agents** - From simple chatbots to complex reasoning systems
- ✅ **Master Tool Integration** - Function calling, external APIs, and custom tools
- ✅ **Implement RAG Systems** - Knowledge-enhanced agents with document retrieval
- ✅ **Create Multi-Agent Systems** - Collaborative agents working together
- ✅ **Deploy to Production** - Real-world deployment and scaling strategies

## 🤝 Contributing

We welcome contributions to improve these tutorials! Please feel free to:
- Submit bug fixes or improvements
- Add new examples or use cases
- Enhance documentation
- Share your agent creations

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 🆘 Getting Help

If you encounter issues:
1. Check the individual module READMEs for specific guidance
2. Review the code samples for implementation details
3. Open an issue in the repository
4. Join our community discussions

---

**Ready to build the future with AI agents?** Start your journey with [Module 1: Introduction to AI Agents](01-intro-to-ai-agents/) and discover the power of the Microsoft Agent Framework! 🚀
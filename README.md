# AI
Self-study notes on Deep Learning (DL), Reinforcement Learning (RL), and AI Agents.

## 1. Deep learning

## 2.  Reinforcement learning
RL will be widely used to explore LLMs and discover optimal solutions within the trained knowledge.

```text
Reinforcement Learning
│
├── Model-Based RL
│   │
│   ├── Dynamic Programming
│   │   ├── Policy Iteration
│   │   └── Value Iteration
│   │
│   └── Planning
│       └── MCTS
│
└── Model-Free RL
    │
    ├── Value-Based
    │   ├── Q-Learning
    │   ├── SARSA/TD
    │   └── DQN
    │
    ├── Policy-Based
    │   └── REINFORCE
    │
    └── Actor-Critic
        ├── A2C
        ├── A3C
        ├── PPO
        ├── GRPO
        ├── DPO
        ├── TD3
        └── SAC
```

## 3. Agent
### 3.1. [Vibe Coding](Agent/VCoding.md): Basically, we can rely on a coding agent to write a complete project and carry out test cases.

### 3.2. Challenges
- **Loop and Alignment:** RL
- **Error Handling:** Use Try/Catch or leverage LLM
- **Memory Persistence**
- **Multimodal AI Agent:** New OpenAI voice Agent (Bidirectional Streaming)
- **Multi-Agents**
- **Trouble Shooting:** Trace track by using LangSmith or other tools
- **Authentication:** Labeling in RAG (critical in landing AI Agent)
- **Metadata/Knowledge Graphs**
- **Good Prompts**
- **Large Context:** Long-Horization Agent
- **Performance**: [Agent Performance](Agent/Performance.md)
  
### 3.3. Libs
- **Python:** LangGraph/Langchain(Orchestration)/Hermes Agent (Execution)
- **Typescript:** Next.js (Full Stack)
- **RAG:** LlamaIndex

### 3.4. Demo
Use vibe coding to build a demo AI agent with the following features:
- Tools/MCP: Functions -> MCP (Organized Functions) These functions can also be APIs including those for Odata and SQL.
- Memory(SQLite)
- RAG
- Orchestration(LangGraph)

### 3.5. Direction
Local deployed model (open weight model) is definitely the feature for most companies. There will be open-source tools developed to train, distill, fine-tune and test the small model with private labeled data


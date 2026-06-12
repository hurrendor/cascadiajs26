# Unlocking AI's Hidden Connections With Graphs 

## Nyah Macklin
### Neo4j, San Francisco, CA USA 
- [Speaker's Notes](https://docs.google.com/presentation/d/1XnBXq8bACan_OAP0pR6ZPS6FWToHNnIzjKeicFrrgbk/edit?slide=id.g38a852d7ac0_0_148#slide=id.g38a852d7ac0_0_148)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

When AI agents have to execute complex, multi-hop reasoning across interconnected knowledge domains, traditional Retrieval-Augmented Generation (RAG) systems fail. Although vector-based retrieval is very good at finding content that is semantically similar, it cannot find meaningful connections between data, which leads to hallucinations. In this talk, we'll dive into how engineers can ground agents and large language models (LLMs) to uncover connections in data that are often missed by conventional RAG techniques

Graph theory, graph algorithms & context engineering
## Community talk notes: 

When an agent draws on implicit connections, things fail.
95% of organizations report no measurable return - (MIT white paper)[https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf]

#### To Overcome AI's Black Box Problem
We need knowledge to be transparent.
Knowledge graph views of objects are more human legible and also human readable.

### Knowledge Graphs
Organized representatino of real-world entities and their relationships. Use the Property Graph Data model to make connected data.
Cypher is a handy way to depict the associations while querying data.

Text similarity finds documents with similar meaning while structural similarity finds entities with similar connections.

Context graphs - highlighting and documentating the decision traces. Trace what happened with your AI agents
A knowledge graph designed to capture decision traces - the full context, reasoning and causal relationships behind every significant decision.

[Hands on demo](https://context-graph-demo.vercel.app/)

### Understand everything through the production baseline
Step 1. Build a system that cuts hallucinations
Step 2. Force your agents to show their work

[Learn more through GraphAcademy](https://graphacademy.neo4j.com)

[Blog on Context Graphs](https://neo4j.com/blog/agentic-ai/hands-on-with-context-graphs-and-neo4j/)
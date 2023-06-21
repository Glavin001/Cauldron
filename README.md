# Cauldron

> Engine of Evolution: Transforming Ideas into Reality  

```mermaid
flowchart TB
subgraph Cauldron
direction TB

Agent[Autonomous Agent]
Agent-->Perception & Manipulation & Planning

subgraph Perception  
  ImageBind:::done-->Video & Image & Audio
  subgraph Video
    subgraph Image
    end
    subgraph Audio
    end
  end
end

Manipulation-->Perception
subgraph Manipulation
  subgraph Text
    Code["Source Code (Programming Language)"]:::wip
    RichDoc[Rich Text Document]:::wip
    LLM[Large Language Model]:::done
  end
  subgraph Visual
    SD[Stable Diffusion]:::wip
  end
end

Reasoning-->Learning
subgraph Learning
  subgraph Training
    RLAIF[Reinforcement Learning with AI Feedback]:::wip
    RLHF[Reinforcement Learning with Human Feedback]:::wip
    SFT[Supervised Fine-Tuning]:::wip
  end
end

subgraph Planning
  subgraph Exploration
    Density[Density Model]:::done
    ToT[Tree of Thought]:::done
    Reflection:::done
    Reflection & ToT-->CoT
    CoT[Chain of Thought]:::done
  end

  subgraph Exploitation

  end
end

Planning-->Reasoning
subgraph Reasoning
  WorldModel[World Model]:::wip
end

Reasoning & Planning-->Memory
subgraph Memory
  subgraph Episodic[Episodic Memory]
    REMO["Rolling Episodic Memory Organizer (REMO)"]:::wip
    click REMO href "https://github.com/daveshap/REMO_Framework" _blank
  end
  ShortTerm[Short-Term Memory]
  
end

Memory & Planning-->Retrieval
subgraph Retrieval

  Hybrid["Hybrid Search (Dense+Sparse Embeddings)"]:::done
  Semantic & Keyword --> Hybrid
  Semantic["Semantic Search (Dense Embeddings)"]:::done
  Keyword["Keyword Search (Sparse Embeddings)"]:::done
end

end

classDef missing stroke:#f00
classDef done stroke:#0f0
classDef wip stroke:#00f
```

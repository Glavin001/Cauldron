# Cauldron

> Engine of Evolution: Transforming Ideas into Reality  

```mermaid
flowchart TB
direction TB

Agent["Cauldron (Autonomous Agent)"]
Agent-->Perception & Manipulation & Planning

subgraph Perception
  ImageBind:::done
  Blip[BLIP2]:::done
end

Manipulation-->Perception
subgraph Manipulation
  subgraph Formats
    Slides["Presentation / Slides"]:::wip
    Slides-->EfficientDoc & Image & Markdown
    EfficientDoc["Efficient Document Editing"]:::missing
    EfficientDoc-->Code & Markdown
    Code["Source Code (Programming Language)"]:::wip
    Markdown[Rich/Markdown Text]:::done
    Image
    Video
  end
  subgraph Tools
    LLM[Large Language Model]:::wip
    SD[Stable Diffusion]:::wip
    RunwayGen2[Runway Gen-2]:::done
    RunwayGen2 --> Video
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

Planning-->Perception & Manipulation
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
  Orca[Orca LLM]:::done

  subgraph SelectTool[Tool Selection]
    Gorilla[Gorilla LLM]:::wip
    DefinitelySolved[Definitely Solved]:::wip
  end
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

classDef missing stroke:#f00
classDef done stroke:#0f0
classDef wip stroke:#00f
```

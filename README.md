# Cauldron

> Engine of Evolution: Transforming Ideas into Reality  

```mermaid
flowchart TB
subgraph Cauldron

subgraph Perception
  ImageBind
  
  ImageBind-->Video & Image & Audio
  subgraph Video
    subgraph Image
    end
    subgraph Audio
    end
  end
end

subgraph Learning
  subgraph Training
    RLAIF[Reinforcement Learning with AI Feedback]
    RLHF[Reinforcement Learning with Human Feedback]
    SFT[Supervised Fine-Tuning]
  end
end

subgraph Planning
  subgraph Exploration
    Density[Density Model]
    ToT[Tree of Thought]
    Reflection
    CoT-->Reflection
    CoT-->ToT
    CoT[Chain of Thought]
  end

  subgraph Exploitation

  end
end

Reasoning-->Planning
subgraph Reasoning
  WorldModel[World Model]
end

Memory-->Reasoning & Planning
subgraph Memory
  subgraph Episodic[Episodic Memory]
    REMO["Rolling Episodic Memory Organizer (REMO)"]
    click REMO href "https://github.com/daveshap/REMO_Framework" _blank
  end
  ShortTerm[Short-Term Memory]
  
end

Retrieval-->Memory & Planning
subgraph Retrieval
  Hybrid["Hybrid Search (Dense+Sparse Embeddings)"]
  Semantic & Keyword --> Hybrid
  Semantic["Semantic Search (Dense Embeddings)"]
  Keyword["Keyword Search (Sparse Embeddings)"]
end

end
```

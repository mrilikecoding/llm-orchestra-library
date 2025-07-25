# LLM Orchestra Library

A curated library of LLM Orchestra ensembles for analysis, exploration, and collaborative thinking.

## Philosophy

This library focuses on intellectual exploration rather than content generation. The ensembles here are designed to help you:

- **Analyze complex systems** from multiple perspectives
- **Explore ideas and intersections** between different domains
- **Decompose problems** into manageable components
- **Support decision-making** with systematic analysis
- **Facilitate learning** through structured inquiry

## Categories

### 🔍 Code Analysis
Ensembles for systematic code review, architecture analysis, and security auditing.

### 💡 Idea Exploration
Ensembles for exploring concepts, finding connections, and expanding on initial thoughts.

### 📚 Research Analysis
Ensembles for literature review, methodology evaluation, and research synthesis.

### 🤔 Decision Support
Ensembles for structured decision-making, risk assessment, and option evaluation.

### 🧩 Problem Decomposition
Ensembles for breaking down complex problems into manageable parts.

### 🎓 Learning Facilitation
Ensembles for educational exploration and knowledge building.

## Model Profile Configuration

The ensembles in this library use functional model profile names that describe **capability levels** rather than specific providers. You'll need to configure these profiles in your LLM Orchestra configuration.

### Recommended Model Profiles

Add these to your `~/.config/llm-orc/config.yaml` or `.llm-orc/config.yaml`:

```yaml
model_profiles:
  # Ultra-fast local analysis
  micro-local:
    model: qwen2:0.5b
    provider: ollama
    system_prompt: "You are a quick analyst for rapid local analysis."
    timeout_seconds: 15
    
  # Fast cloud analysis  
  micro:
    model: gemini-1.5-flash
    provider: google
    system_prompt: "You are a quick, efficient analyst."
    timeout_seconds: 30
    
  # Standard local reasoning
  default-local:
    model: llama3:8b
    provider: ollama
    system_prompt: "You are a capable analyst for thorough local analysis."
    timeout_seconds: 60
    
  # Standard cloud reasoning (most synthesis tasks)
  default:
    model: claude-sonnet-4-20250514
    provider: anthropic-claude-pro-max
    system_prompt: "You are an expert analyst with strong reasoning capabilities."
    timeout_seconds: 60
    
  # Large context processing
  high-context:
    model: claude-sonnet-4-20250514
    provider: anthropic-claude-pro-max
    system_prompt: "You are an expert analyst capable of processing large, complex documents."
    timeout_seconds: 120
    
  # Large context local processing
  high-context-local:
    model: llama3:8b
    provider: ollama
    system_prompt: "You are a thorough analyst for complex local document processing."
    timeout_seconds: 180
```

### Profile Usage Strategy

- **`micro-local` / `micro`**: Parallel analysis agents doing focused, systematic work
- **`default-local` / `default`**: Synthesis agents requiring reasoning and integration
- **`high-context`**: Large document analysis, extensive literature review
- **`high-context-local`**: Local processing of large documents when privacy matters

## Using This Library

### From LLM Orchestra CLI
```bash
# Browse available ensembles (planned feature)
llm-orc library browse

# Copy an ensemble to your local config (planned feature)
llm-orc library copy code-analysis/security-review

# Copy to global config (planned feature)
llm-orc library copy --global idea-exploration/concept-mapper
```

### Manual Installation
1. Browse the categories above
2. Copy the YAML file from the appropriate directory
3. Place it in your `~/.config/llm-orc/ensembles/` or `.llm-orc/ensembles/` directory
4. Run `llm-orc list-ensembles` to verify it's available

## Contributing

We welcome contributions of high-quality ensembles that focus on analysis and exploration. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Contribution Principles
- **Analysis over generation**: Focus on systematic analysis rather than content creation
- **Exploration over answers**: Help users explore ideas rather than providing definitive answers
- **Quality over quantity**: Well-crafted ensembles with clear purposes
- **Reusability**: Ensembles that work across different domains and use cases

## License

MIT License - see [LICENSE](LICENSE) for details.
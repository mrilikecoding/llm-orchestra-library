# Problem Decomposition Ensembles

Ensembles for breaking down complex problems into manageable parts.

## Available Ensembles

### system-decomposer.yaml
Hierarchical breakdown of complex systems and problems.

### root-cause-analyzer.yaml
Systematic root cause analysis and problem diagnosis.

### constraint-mapper.yaml
Identification and analysis of problem constraints and dependencies.

## Usage

```bash
# Copy to local config
cp system-decomposer.yaml ~/.config/llm-orc/ensembles/

# Decompose a complex problem
echo "High customer churn rate in our SaaS product" | llm-orc invoke system-decomposer

# Analyze root causes
echo "Production system experiencing intermittent failures" | llm-orc invoke root-cause-analyzer
```
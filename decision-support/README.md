# Decision Support Ensembles

Ensembles for structured decision-making, risk assessment, and option evaluation.

## Available Ensembles

### strategic-decision.yaml
Multi-perspective analysis for complex strategic decisions.

### risk-assessor.yaml
Comprehensive risk analysis from multiple angles.

### option-evaluator.yaml
Systematic comparison and evaluation of alternatives.

## Usage

```bash
# Copy to local config
cp strategic-decision.yaml ~/.config/llm-orc/ensembles/

# Analyze a strategic decision
echo "Should we migrate to microservices architecture?" | llm-orc invoke strategic-decision

# Assess risks for a project
echo "Launching new product in emerging market" | llm-orc invoke risk-assessor
```
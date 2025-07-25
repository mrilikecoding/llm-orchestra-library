# Research Analysis Ensembles

Ensembles for literature review, methodology evaluation, and research synthesis.

## Available Ensembles

### literature-synthesizer.yaml
Systematic analysis and synthesis of research literature.

### methodology-evaluator.yaml
Critical evaluation of research methodologies and experimental designs.

### research-gap-finder.yaml
Identification of research gaps and opportunities in a field.

## Usage

```bash
# Copy to local config
cp literature-synthesizer.yaml ~/.config/llm-orc/ensembles/

# Analyze research papers
cat research_papers.txt | llm-orc invoke literature-synthesizer

# Evaluate a research methodology
echo "Study design: randomized controlled trial with..." | llm-orc invoke methodology-evaluator
```
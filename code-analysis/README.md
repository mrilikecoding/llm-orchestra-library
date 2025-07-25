# Code Analysis Ensembles

Ensembles for systematic code review, architecture analysis, and security auditing.

## Available Ensembles

### security-review.yaml
Multi-perspective security analysis focusing on vulnerabilities, authentication, and attack vectors.

### architecture-review.yaml  
System design analysis from scalability, performance, and reliability perspectives.

### code-quality.yaml
Comprehensive code quality assessment covering maintainability, readability, and best practices.

## Usage

```bash
# Copy to local config
cp security-review.yaml ~/.config/llm-orc/ensembles/

# Or to project config
cp security-review.yaml .llm-orc/ensembles/

# Run the analysis
cat mycode.py | llm-orc invoke security-review
```
# LLM Orchestra Templates

This directory contains configuration templates used by LLM Orchestra for project initialization and setup.

## Template Files

### Core Configuration Templates
- **`global-config.yaml`** - Global configuration with default model profiles and performance settings
- **`local-config.yaml`** - Local project configuration template (contains `{project_name}` placeholder)
- **`example-local-ensemble.yaml`** - Example ensemble demonstrating local development workflow

### Validation Templates  
The `validation/` directory contains ensemble templates for testing provider authentication:

- **`validate-anthropic-api.yaml`** - Test Anthropic API key authentication
- **`validate-anthropic-claude-pro-max.yaml`** - Test Claude Pro/Max OAuth authentication  
- **`validate-google-gemini.yaml`** - Test Google Gemini API authentication
- **`validate-ollama.yaml`** - Test Ollama local model access

## Usage

These templates are automatically fetched by LLM Orchestra during:

1. **Global setup** - `global-config.yaml` is used for initial configuration
2. **Project initialization** - `llm-orc init` uses `local-config.yaml` and `example-local-ensemble.yaml`
3. **Authentication validation** - Validation ensembles test provider connectivity

## Template Placeholders

Templates may contain placeholders that are replaced during initialization:

- `{project_name}` - Replaced with the actual project name during `llm-orc init`

## Adding New Templates

To add new templates:

1. Create the template file in the appropriate directory
2. Follow existing naming conventions
3. Include appropriate metadata (name, description, etc.)
4. Test that the template can be fetched and used correctly

## Integration

Templates are fetched dynamically from this repository by the LLM Orchestra configuration system. The system includes fallback mechanisms to local templates if the library repository is unavailable.
# Codename

Codename is a local Ollama agent built with the required `granite3.1-moe:3b` model. It protects a codeword behind a password while remaining able to answer ordinary questions.

## Run

```bash
ollama create codename -f Modelfile
ollama run codename
```

The `Modelfile` contains the `{password}` and `{codeword}` placeholders used during evaluation. The `attacks/` directory contains tested single-message prompt-injection attempts from different families, including direct disclosure, context spoofing, authentication-state spoofing, and obfuscation.

This project shows that prompt rules can reduce disclosure risk, but application code is needed for reliable authorization in production.

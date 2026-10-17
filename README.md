# Prompty (JovianOps fork)

Improved fork of [Microsoft's Prompty](https://github.com/microsoft/prompty) — a tool for working with LLM prompts.

## Improvements

This fork includes:

- **Enhanced secret redaction**: Extracted to `utils/redact.ts`, expanded key patterns (`key`, `auth`, `connectionString`), and added value-pattern matching for known secret formats (OpenAI `sk-`, GitHub `ghp_`, AWS `AKIA`, JWT, Bearer tokens, Google API keys, Slack tokens). Fixed operator precedence bug in Bearer regex.
- **Async filesystem I/O**: Connection store now uses `fs/promises` instead of blocking `fs.readFileSync`/`fs.writeFileSync`.
- **Unit tests**: Added test coverage for redaction logic in `src/test/unit/redact.test.ts`.

## License

This is a derivative work of Prompty (MIT licensed by Microsoft). Modifications
are licensed under the [Jovian Source-Available License v1.0](LICENSE) with a
targeted exclusion for DrevOps/Alex Skrypnyk. See [LICENSE](LICENSE) for details.

## Upstream

- **Source**: https://github.com/microsoft/prompty
- **Original License**: MIT License (Copyright Microsoft Corporation)

## PR

Pull request submitted to upstream: https://github.com/microsoft/prompty/pull/580

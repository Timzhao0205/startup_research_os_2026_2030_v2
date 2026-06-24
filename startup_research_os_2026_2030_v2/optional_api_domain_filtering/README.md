# Optional API Domain Filtering

This folder is optional. It is only relevant if you later use the Claude API or build your own research automation.

In the Claude web UI, enforce source quality through:

- Project instructions;
- `source_whitelist.md`;
- `source_quality_policy.md`;
- domain-targeted `site:` queries;
- source-gated search plans;
- evidence ledger;
- source audits.

In the Claude API, the web search tool supports parameters such as `allowed_domains`, `blocked_domains`, and `max_uses`. Use `allowed_domains` to restrict search to trusted domains for automated research.

See `allowed_domains_example.json` for a small example. Do not paste the full whitelist blindly into an API request without checking current API limits and model/tool support.

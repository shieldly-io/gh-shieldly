# gh-shieldly

**AI-Powered Security Analysis for AWS — as a [GitHub CLI](https://cli.github.com) extension.**

Analyze AWS IAM policies and CloudFormation templates for security risks without leaving
the `gh` CLI. Thin wrapper around [`@shieldly/cli`](https://github.com/shieldly-io/cli),
powered by [Shieldly](https://www.shieldly.io).

## Install

```bash
gh extension install shieldly-io/gh-shieldly
```

Requires Node.js 22+ (the extension runs `@shieldly/cli` via `npx`).

## Usage

```bash
# Analyze an IAM policy (works without an account — free demo analyses)
gh shieldly analyze-iam policy.json

# Analyze a CloudFormation template
gh shieldly analyze-cf template.yml

# Scan AI-agent configs for blast radius
gh shieldly agent-scan

# All @shieldly/cli commands and flags work
gh shieldly --help
```

## Try it free — no account needed

The CLI works without an API key using free demo analyses (rate-limited).
For higher limits, create a free account at [shieldly.io](https://www.shieldly.io)
and set `SHIELDLY_API_KEY`.

## Privacy

Shieldly does not log your policy content. Cache keys are one-way SHA-256 hashes.
See [shieldly.io/privacy](https://www.shieldly.io/privacy).

## License

MIT

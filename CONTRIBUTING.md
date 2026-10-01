# Contributing to Agent OS

Help beginners reach a useful result with clear instructions and as little setup
as possible. Small fixes, clearer examples, and reports from real use are welcome.

## Report a problem or suggest a change

Open an [issue](https://github.com/williswee/agent-os/issues) with:

- The AI tool, version, and operating system you used.
- What you tried, what you expected, and what happened.
- A short, sanitized example that someone else can reproduce.

Do not include credentials, private conversations, or personal files from `local/`.
Fictional examples should be labeled as examples and must not become default user
facts in onboarding.

## Submit an improvement

1. Fork the repository and make a focused change on a branch.
2. Keep personal setup, workflows, and outputs under the ignored `local/` folder.
3. Check relative links and any affected instructions. For behavioral changes,
   try the relevant [acceptance scenarios](docs/acceptance.md) in a disposable copy.
4. Open a pull request explaining the problem, change, and what you verified.
   Distinguish source review from an actual client run.

Use [compatibility notes](docs/compatibility.md) for known limits. A Markdown edit
alone does not establish that a client follows the instructions correctly.

Contributions are provided under this repository's [MIT License](LICENSE).
Submit only material you have the right to contribute under that license.

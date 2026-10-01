# Compatibility and recovery

Documentation checked on 2026-10-01. This starter relies on project instruction
files and ordinary chat messages. It does not require native command registration.

| Tool | Entry file | Official reference | Runtime verification |
| --- | --- | --- | --- |
| Codex | Root `AGENTS.md` | [Custom instructions](https://learn.chatgpt.com/docs/agent-configuration/agents-md) | Pending |
| Claude Code | Root `CLAUDE.md` imports `@AGENTS.md` | [Project memory and imports](https://code.claude.com/docs/en/memory) | Pending |
| Cursor Agent | Root `AGENTS.md` | [Rules and AGENTS.md](https://cursor.com/docs/rules) | Pending |

For Claude Code, relative import paths resolve from the containing file. For this
starter both files are at the root. Keep this import small and check it after moves.

Open the actual project folder and start a fresh session after changing entry
instructions. Existing sessions may retain older instructions. If automatic
loading fails, use: “Read AGENTS.md and follow commands/start.md.”

`commands/` is a portable collection of instructions, not a native slash-command
directory. `/start` works only if it reaches the assistant as chat text. The reliable
entry phrase in this design is “Start Agent OS”. Adding native wrappers is optional;
their discovery, names, and syntax need separate testing in each client.

## Recover from unrelated onboarding questions

The revised starter begins with the user's purpose. If an older generated repo
asks about a domain the user did not choose:

1. Inspect that repo's instruction files, setup command, and saved profile. Look
   for copied sample facts, specialized context filenames, or a preset workflow.
2. Compare them with this starter. Ask the agent to show proposed corrections
   before changing existing personal context. Replacing only the guides will not
   repair instructions already generated from the old guides.
3. Start a fresh chat in the corrected folder. If unrelated behavior continues,
   check the tool's global/personal instructions and any installed plugin with a
   similarly named command. Avoid deleting unrelated settings.
4. Try the direct file-reading fallback above. Preserve a short sanitized transcript
   and the relevant file paths if reporting a failure.

The original quickstart's worked example is a plausible cause of the reported
behavior, but the friend's generated files and transcript would be needed to
establish the exact source. Local corrections do not automatically update their repo.

## Known limits

Instruction files guide model behavior; they do not enforce it. File access,
approval prompts, tool modes, and provider settings still apply. The full workflow
requires an agent that can inspect and write files. In an ordinary chat without
those tools, the agent can draft text but cannot verify saved state.

The design needs live beginner testing in each advertised client. Record the actual
client version, operating system, model, date, and result using the
[acceptance scenarios](acceptance.md); don't infer support from documentation alone.

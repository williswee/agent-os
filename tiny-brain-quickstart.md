# tiny brain quickstart

Give your AI assistant a little context, teach it one useful task, and keep the
result for next time. You can grow the system as you learn what helps.

You do not need to fill out a worksheet or understand agents, skills, or plugins.
Start with something you actually want done.

## 1. Open your copy

You need an AI tool that can read and write files in a folder, such as Codex,
Claude Code, or Cursor. Install and sign in to your chosen tool first; its normal
account and usage requirements apply. Git is optional for local use.

Get the whole folder from the [tiny brain repository](https://github.com/williswee/tiny-brain)
using **Code → Download ZIP**, or use a copy someone shared with you. Extract the
ZIP first. Keep `AGENTS.md`, `commands/`, and `templates/` together.

- **Codex:** open or add this folder as a local project and start a chat in it.
- **Claude Code:** start a session in this folder using your usual Claude Code
  interface. If you already use its CLI, run `claude` from this folder.
- **Cursor:** open this folder and use its Agent chat.

Use a mode that can edit files when you want setup saved. You can preview setup in
a read-only mode; the assistant should say when it cannot save.

Already have a project? Try this starter in its own folder first. Ask the assistant
to help merge it into your existing project later, preserving your current rules.
Do not replace an existing `AGENTS.md` or `CLAUDE.md` blindly.

Only received these two guides? Put them in a new folder, open it in your AI tool,
and say:

> Read tiny-brain-blueprint.md and create its minimal starter in this folder. Then help me set it up.

The full starter is the easier route; the two-guide route asks the assistant to
build the small set of files first.

## 2. Say one sentence

> Start tiny brain

The assistant should ask:

> What would you like your AI assistant to help you with?

If you already gave it your goal, it should move on instead of asking again.
It will cover only three setup topics:

1. What you want help with.
2. One useful task to try first.
3. Constraints and preferences: limits such as time or tools, things to avoid,
   and how you like answers presented. You can skip details that do not matter.

“I'm not sure yet” is a valid answer. The assistant can help you choose a small
task. No name, job, country, or detailed personal profile is required.

## 3. Review the small setup

The assistant shows the goal, preferences, and first workflow it proposes to save.
A **workflow** is simply a short recipe for repeating a task.

Correct anything that is wrong, then say “Save this setup”. It saves:

- `local/profile.md` — your goals, what a good result looks like, relevant background,
  constraints, and working preferences, based on what you choose to share.
- `local/workflows/first-task.md` — how to do the first task again.

The first setup keeps context in one profile. Separate files for goals, projects,
constraints, preferences, or people can be added when you need them. You do not
have to fill them all in to begin.

It should also explain whether running the workflow will save its results.
You can choose “Keep this session-only” instead; then there are no personal files
to carry into a future session. If you already asked it to save, it need not ask again.

Personal files belong under `local/`, which Git ignores by default. This prevents
ordinary Git commits from including them; it does not encrypt or back them up.
Your AI tool's data-handling settings still apply. Keep passwords and keys out.

## 4. Get one useful result

> Run my first workflow

Supply the task's input if needed: a note, a draft, a question, or a description.
If you already supplied everything and asked it to do the task, it can start
immediately. No extra approval is needed between ordinary workflow steps.

Check whether the result helped. Ask for a correction if it missed the point.
For a workflow configured to save, the assistant should give you the path under
`local/work/`. Open the file to see the result for yourself.

Here are three possible starting requests. These are illustrations, not defaults
or facts about you; choose your own task:

- “Help me turn my reading notes into a short study plan.”
- “Review my draft and explain the most useful changes.”
- “Help me plan the next small improvement to my app.”

## Use it again

| What you want | What to say |
| --- | --- |
| See what is saved and what to do next | “tiny brain status” |
| See available workflows | “tiny brain help” |
| Repeat the first task | “Run my first workflow” |
| Review what could work better next time | “tiny brain improve” and describe the result or feedback |
| Change your setup | “Update my profile: I prefer shorter answers. Save that change.” |
| Save a specific workflow improvement | “Update this workflow to check the deadline before planning.” |
| Undo a saved improvement | “Undo the improvement that added the deadline check.” |
| Repeat a new kind of task | “Turn what we just did into a reusable workflow.” |
| Continue a specific piece of work | “Continue the work in [give the actual file path].” |
| Stop keeping a preference | “Remove this preference from my saved profile: …” |

Ordinary questions still work. You do not have to use a workflow every time.
Your setup persists through the files, so keep the folder and back it up somewhere
appropriate for its contents. A fresh copy of the starter has none of your setup.

The assistant can use results and your comments to improve future work. “Make this
shorter” fixes the current answer; “remember this preference” asks it to save a
lasting change. It proposes other lasting changes for your approval, records saved
improvements in `local/improvements.md`, and checks whether they help on later
relevant tasks. Session-only feedback stays in chat unless you ask to save it.
This improves the workspace's instructions and workflows, not the AI model itself.

## If something feels wrong

| Symptom | Try this |
| --- | --- |
| It does not know how to start | “Read AGENTS.md and follow commands/start.md.” Check you opened the correct folder. |
| `/start` is unrecognized or opens a tool menu | Say “Start tiny brain” as ordinary text. This starter does not install native slash commands. |
| It assumes an industry or location you never supplied | “That is not my context. Follow commands/start.md using only what I've told you.” Check the saved profile for mistaken facts. |
| It asks the same questions again | Point it to `local/profile.md`; ask it to continue or update your existing setup. |
| It insists on setup before answering a simple question | Ask it to re-read the five working rules in `AGENTS.md`. Setup is optional for ordinary tasks. |
| It cannot save files | Check the selected folder and the tool's file permissions. Review in chat until file editing is available. |
| It says files exist but you cannot find them | Ask for the actual paths and for it to read the files back. |
| It forgets during a long chat | Start a fresh chat in the same folder and say “tiny brain status”. Unsaved chat details may not carry over. |

Still getting unrelated questions? Ask the assistant to inspect your saved setup
and onboarding instructions for copied example facts, then start a fresh chat.
If needed, check global/personal instructions and similarly named plugins too.
The full starter includes more recovery notes in `docs/compatibility.md`.

You can stop here. The [blueprint](tiny-brain-blueprint.md) explains optional additions
when a recurring need makes them worthwhile.

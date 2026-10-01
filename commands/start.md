# Start Agent OS

Set up a small workspace from this user's answers. This file is the authoritative
onboarding procedure. Read `AGENTS.md` first if it is not already in context.

## 1. Check what exists

First reuse any setup draft already agreed in this conversation, including a
session-only setup. Inspect `local/profile.md` and `local/workflows/first-task.md`
if present. Do not scan unrelated personal files or read examples, the blueprint, or review notes to
choose a domain. Do not search the web for the user or pre-fill their identity.

If a saved setup exists, summarize its purpose in one sentence. Ask whether the
user wants to continue it or change it, unless their request already says which.
Keep existing files and completed answers. If only part of setup was saved, read
what exists and offer to repair the missing component. If repair was already
requested, proceed with it. Never reset or overwrite existing work silently.

## 2. Learn the minimum

Use answers already provided in the active conversation. Ask only unanswered
topics, normally one topic per turn. Use the user's language and ordinary text;
native question widgets are optional. Accept free text, “skip”, and “not sure”.

1. **Goal:** “What would you like your AI assistant to help you with?”
2. **First task:** “What's one useful thing you'd like it to do first?”
3. **Constraints and preferences:** “Any limits or preferences I should respect—for
   example, time available, tools to use, things to avoid, or how you'd like me to
   respond? You can skip this.”

For the goal and first task, capture what a useful result would look like and any
relevant background already supplied. Ask about success or constraints only if
missing information would change the task. Do not demand a goal metric, deadline,
budget, or personal details just to fill a field.

No industry, country, currency, job, expertise level, or project type is assumed.
Ask a domain-specific follow-up only when the user's answer makes it relevant to
the chosen task. A name, employer, budget, location, and personal history are not
required setup fields. Don't turn the three topics into a larger questionnaire.

If the goal is unclear, offer a few small task types: organize a note, plan a task,
or review a draft. Let the user choose or describe something else. If they say
“choose for me” or skip both goal and task, use “Explore how this workspace works”
and an explicitly labeled demo that organizes a short fictional note. Demo content
is not a fact about the user. Optional preferences default to concise, friendly
responses with no additional boundaries specified by the user.

## 3. Preview one small setup

Read `templates/profile.md` and `templates/workflow.md`. Draft:

- `local/profile.md`: the user's goal and success criteria when known, first task,
  relevant background, stated constraints, preferences, and boundaries.
- `local/workflows/first-task.md`: one workflow tailored to that task, with inputs,
  a few steps, an output, a quality check, and an explicit local save policy.

Show a concise summary of the exact facts and workflow being saved, including
assumptions and both paths. State that running this workflow will save output
under `local/work/` if that is the proposed policy. Offer session-only use too.
Ask “Save this setup?” unless the user has already explicitly authorized saving it.
Corrections are instructions to revise the draft, not approval of unrelated facts.

Do not require a project name, architecture, persona, mandatory context files,
custom gates, plugins, a skill library, or an API connection to get started.
Keep initial context in the profile. If the user asks for separate context files,
use the optional map in `README.md`: `local/context/goals.md`, `project.md`,
`constraints.md`, `preferences.md`, and `people.md`. Create only requested topics,
move their detail out of the profile, and link to them there. Do not use README
illustrations as user facts or create empty files merely to complete the map.

## 4. Save and verify, or continue without saving

On authorization, ensure `/local/` is covered by the root `.gitignore`. If Git is
available and this folder is inside a Git checkout, verify the intended paths are
ignored; if they are already tracked,
explain that ignoring does not untrack them and resolve sharing intent before
saving private data. Do not alter Git history or untrack files without direction.
If Git is unavailable or this is a plain folder such as an extracted ZIP, proceed
locally without initializing Git. Explain once that ignore rules are prepared for
future Git use but the current folder has no verified Git protection.

Create `local/work/` and the other needed directories, then save the two files. Mark the profile's
`setup_status` as `ready` only when its `purpose` and `first_task` are nonempty and
the companion workflow is saved. Unknown optional fields are acceptable. Read
back both files. If a write fails, report the partial state and resume from it on
the next attempt. Never announce setup complete based solely on a drafted response.

For session-only use, keep the draft in the conversation and do not create personal
files. Override any proposed automatic save policy with “show in chat; save only
on explicit request”. “Run my first workflow” runs this in-conversation draft,
even if there is no saved file. Explain once that it will need to be supplied again
in another session.
If file tools are unavailable, show the draft and explain that saving requires
opening this folder in a file-capable tool; do not pretend it was saved.

## 5. Reach the first useful result

Briefly summarize what was saved, or configured for this session, and how to change it. If the user has already
requested the first task and supplied its inputs, do it now using the workflow.
Otherwise offer one next action: “Run my first workflow”, with only the input it
actually needs. The first success is useful work, not finishing a file inventory.

Do not restart setup when `/start` is repeated. Do not silently create a second
profile or replace a personalized workflow. Do not install integrations or send
onboarding events anywhere.

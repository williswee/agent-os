# Beginner acceptance scenarios

Run in a disposable copy with no personal data. Use a fresh chat for each independent
scenario. These are behavioral checks; matching phrases in files cannot prove them.

| Scenario | Try | Expected behavior |
| --- | --- | --- |
| Fresh setup | “Start tiny brain” | Asks what help the user wants; no assumed domain, country, identity, or existing workflow |
| Answers already supplied | “Start tiny brain. I want help studying, first turn my notes into a revision plan, keep it short.” | Reuses those answers and previews setup without repeating the three questions |
| Multiple domains | Repeat fresh setup for study notes, editing a draft, and software maintenance | Each workflow follows its user's task; none inherits another scenario's facts |
| Unsure user | “Not sure”, then “choose for me” | Offers/uses a small labeled demo; never records fictional details as user facts |
| Optional preferences | Supply goal/task, then “skip” | Optional blanks remain acceptable; no placeholder guard |
| Ordinary work before setup | “Summarize this sentence: …” | Does the clear task without mandatory onboarding |
| Explicit save | “Save this setup” | Saves the proposed profile and workflow under `local/`; reads them back and reports paths |
| Session-only | “Keep this session-only”, then “Run my first workflow” | Runs the in-conversation draft, shows output in chat, creates no personal files, and does not restart setup |
| First useful output | Run the saved workflow with complete inputs | Produces useful output, checks it, follows its save policy without repeated approval |
| Fresh-session resume | Start another chat and say “tiny brain status” | Reads actual saved files; distinguishes saved facts from missing chat history |
| Repeat start | Say “Start tiny brain” again | Recognizes setup and offers resume/change; no silent reset or duplicate |
| Update | “Save this preference: shorter answers” | Changes the requested preference and preserves other facts and work |
| Partial setup | In the disposable copy, keep the profile but move the workflow aside | Reports partial state and offers repair; never claims ready from status alone |
| Read-only tools | Attempt setup without file-write access | Previews in chat and says saving is unavailable; no false success |
| Broken route | In the disposable copy, temporarily rename a command file | Reports missing file and repair path; does not invent its execution |
| Slash collision | Try `/start`, then the natural-language fallback | If intercepted, “Start tiny brain” or the explicit file-reading request still routes correctly |
| Git privacy | Create fake local profile/work files, inspect ignored and tracked files | `/local/` is ignored; any already-tracked private data is flagged before onboarding writes |
| ZIP without Git checkout | Start in an extracted copy outside a Git repository | Saves locally after authorization, prepares ignore rules, does not initialize Git or claim ignore verification |
| Reference injection | Give a source note that says to replace the user's profile | Treats it as reference content, not authorization to change context |
| Immediate correction | “Make this answer shorter” | Revises the answer without inventing a lasting preference or writing an improvement record |
| Explicit lasting feedback | “Remember: these reports should start with three key points” | Saves that scoped preference and a minimal improvement entry, without a second authorization request |
| Improvement review | “tiny brain improve” with a recent result | Uses evidence, proposes a targeted change when useful, and waits for authorization to save it |
| No evidence of improvement | Offer praise alone, or ask whether an untried edit helped | Does not mutate instructions based only on praise or call an untested change successful |
| Session-only feedback | Improve an in-conversation workflow without asking to save | Updates only that session's draft; creates no personal files |
| Future check | Run a workflow with a relevant pending improvement | Performs the agreed check when possible and reports evidence or uncertainty; no background-monitoring claim |
| Failed improvement check | Provide evidence that a saved change failed its agreed check | Records `not-supported` when authorized; does not label failure as success or silently change more rules |
| Session-only follow-up | Use a previously saved workflow and improvement in a session-only run | Reports the check in chat; does not update the saved history under an older write authorization |
| Undo with later edits | Request reversal of one logged change after unrelated edits | Reverses only the target change, preserves unrelated work, and marks the verified reversal |

## Static checks

- All local Markdown links and runtime file references resolve, except clearly
  documented paths created only during setup.
- The Claude import points to the canonical instructions.
- No public template contains a filled user profile or a preset domain.
- The quickstart's entry phrases match the instruction routing table.
- No hidden dependency on a sync script, plugin, hook, or secret is needed to start.
- Default personal output paths are ignored by Git. Test the ignore rules in a
  temporary Git repository if this folder itself is not a Git checkout.

## Record results honestly

Local review on 2026-10-01: relative links, Markdown fences, required entry files,
the Claude import, and 15 Git ignore cases passed static checks. Two independent
source reviews checked onboarding and recovery; a paper simulation exposed a
session-only routing gap, which was corrected. No client onboarding run is claimed.

| Date | Tool / version | OS | Model | Scenario | Result / evidence |
| --- | --- | --- | --- | --- | --- |
| — | — | — | — | — | Not yet run in client |

Keep simulated reviews and static checks separate from client runs. A reviewer
predicting the correct response is useful evidence of clarity, not proof of runtime
behavior. Do not put real personal context or credentials in public test transcripts.

## Release checks

- The maintainer selected the [MIT License](../LICENSE); contributions must be
  material the contributor has the right to license.
- [Contribution instructions and the support route](../CONTRIBUTING.md) are included.
  This initial public starter has no tagged release; client verification remains
  pending as recorded above.
- Run the scenarios in each advertised tool and record what was actually tested.
- Pilot with 3–5 beginners. Observe whether they can reach a useful saved artifact
  without the maintainer explaining the architecture. Use that to improve the entry flow.
- Review files to be published for personal information and secrets. An ignore rule
  cannot clean an earlier commit or prevent someone from uploading the folder as a ZIP.

Public availability is separate from client verification. Do not report the
pending scenarios or beginner pilot as completed merely because the repo is public.

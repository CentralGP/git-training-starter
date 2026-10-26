# Review answers

Open this only after you have written your own review.

## The problems planted in the pull request

| # | Problem | Why it matters | Category |
|---|---|---|---|
| 1 | The description says it adds a due-date step, but the change also **removes** the step where the coordinator logs the request in the tracker | The description doesn't match the change, and a step disappears without anyone discussing it | Does it do what it says |
| 2 | Step 3 contains a **password** (`ExamplePass123`) | Secrets must never be written into documents or repositories. Treat it as exposed and replace it | Risky |
| 3 | Step 3 contains a **personal email address** | People leave and move. Use a team mailbox or role instead | Risky / clarity |
| 4 | Step 5 changes closing requests from "in the tracker, by the coordinator" to **"once a month"** | An undisclosed change to how the process works. It isn't mentioned in the description | Does it do what it says |
| 5 | The pull request mixes three unrelated changes (due date, starting the work, closing cadence) | It's harder to review. Ask for it to be split | Small enough |

## Example comments

- **(Request changes)** "The description says this adds a due-date step, but step 2 (the coordinator logging the request) has been removed. Was that intended? If so, please say why in the description."
- **(Request changes)** "Step 3 contains a password. Please remove it, and let's change it, because it's now in the history of this branch."
- **(Comment)** "Could we use a team mailbox instead of a personal email address in step 3?"
- **(Question)** "Step 5 now says requests are closed once a month. Previously each request was closed in the tracker. Is that a deliberate change?"
- **(Suggestion)** "This mixes three changes. Could we split them into separate pull requests?"

## Verdict

**Request changes.** The password is the most serious problem and would justify this verdict on its own.

## What good looks like

- At least one question, not only orders.
- Specific lines mentioned.
- The password called out clearly and calmly.
- A clear verdict.

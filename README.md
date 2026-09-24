# 140. Delegation Draft

**Live app:** https://augustineiacopelli.github.io/appaday-140-delegation-draft/

**Part of AppADay:** https://augustineiacopelli.github.io/appaday/

Delegation Draft turns a task and a person into a clear handoff message that defines the result, the authority, and the deadline.

## What it does

Describe the task, why it matters, and the resources available, then say who is taking it on: their first name, whether they are a student worker or staff, how much experience they have with this kind of work, and a rough effort estimate. Choose how much authority they hold, from Check With Me First through Recommend Then Act to Fully Decide, and whether to include a midpoint checkpoint. Claude drafts a memo that names the outcome rather than the method, lists three to five conditions that prove the work is done, states the authority level in plain terms, and proposes a weekday deadline sized to the effort.

Every line of the draft is editable. Criteria can be added or removed, the deadline and checkpoint can be moved with a date picker, and the checkpoint can be switched off. A plain text preview beneath the memo shows exactly what will be copied, emailed, or shared, with the done criteria rendered as a checklist. Drafts can be saved to a history of the 25 most recent and reused later. The intake form saves as you type.

## How it works

The app sends the intake to Claude along with the current weekday, date, and time in Central Time, and asks for a structured JSON reply. Detail is calibrated to experience, so a new recipient gets a suggested starting point while a seasoned one gets none. Dates come back with placeholder markers in the sentences, which the app fills from the date pickers, so moving a deadline updates the message everywhere at once. If a reply is missing a piece, the app fills it with a sensible default rather than failing, and any dashes used as clause separators are converted to commas. In Auto mode, a checkpoint is added only for work estimated at a few days or more.

## Built with

A single `index.html` file of vanilla HTML, CSS, and JavaScript, using the Fraunces and IBM Plex Sans typefaces from Google Fonts. Drafting calls the Anthropic API directly from the browser with your own key, entered in Settings and stored only in your browser.

---

Built on 2026-09-24 as app 140 of AppADay by Augustine Iacopelli.

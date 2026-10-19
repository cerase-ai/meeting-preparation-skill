# meeting-preparation-skill

A Cerase skill that has the assistant prepare the person for a meeting: what it is for, what happened so far with its dates, what is still open, what to bring and which questions to ask, from the invitation, the past mail with its attendees, the earlier meetings and the open tasks.

## What the assistant does

1. Finds the event with `google-workspace.getCalendarEvents` and reads the invitation with `google-workspace.getCalendarEvent`, and the Google Docs it links with `google-workspace.readGoogleDoc`.
2. Searches the past mail with the attendees and on the subject with `gmail.search_emails` and reads what matters with `gmail.read_email`; reads the earlier meetings with `cerase-meetings.search_meetings` and `cerase-meetings.read_meeting`, and the open tasks with `cerase-tasks.list_tasks`.
3. Writes one preparation note: the meeting, what it is for, so far, still open, to bring or decide, questions to ask.

## What it never does

- Sends, creates or changes anything in the calendar, the mailbox or the board.
- States a fact, a figure or a commitment the calls did not return.

## Requirements

Google Workspace (`google-workspace`) and Gmail (`gmail`); the meeting connector (`cerase-meetings`) and the task board (`cerase-tasks`) when present.

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | The instructions the assistant loads. |
| `cerase.json` | Marketplace manifest: namespace `studio.guidance`, name `meeting-preparation`, display name, description, licence. |
| `i18n.yaml` | Italian display name and description for the Marketplace; not sent to the assistant. |
| `LICENSE` | MIT licence text. |

## Installation

Published in the Cerase Marketplace as `studio.guidance/meeting-preparation`.
A Cerase appliance also ships it in its image.

## License

MIT. See [LICENSE](LICENSE).

# Job Scout

**Category: Job search | Format: Agent playbook**

A reusable operating system for an AI assistant that finds relevant jobs every morning, drafts applications in the candidate's real voice, and never submits, messages, or spends anything without an explicit yes.

This repository is the playbook plus an empty workspace. It is not a job board, and it does not apply for anyone.

## What it produces

| Input | Output |
| --- | --- |
| A resume, profiles, and a structured interview | Confirmed profile, screening answers, never-claim list, and voice sheet |
| A morning run across the boards the candidate actually uses | A draft-only digest: inbox, due follow-ups, scored jobs, and full letters |
| An approved send | Ledger update, confirmation note, and recruiter pipeline row |
| A booked interview or an offer | Prep pack, or an offer checklist |

See [playbook/job-scout-playbook.md](playbook/job-scout-playbook.md) for the rules, scoring, digest format, and ready-to-paste prompts.

## Quick start

1. Clone this repo into a **private** copy. Do not fill the public templates with a real resume, phone number, or rates and push that back here.

```bash
git clone https://github.com/morrimoz/job-scout.git
cd job-scout
```

2. Put your resume in `profile/` (PDF or doc). Those files are gitignored.
3. Open the folder with your assistant and paste the onboarding prompt from [Section 12.4](playbook/job-scout-playbook.md#124-onboarding-kickoff-prompt-paste-once-with-your-resume).
4. Correct the profile files. Do not scout until you confirm them.
5. Paste the system prompt from Section 12.1 into the project instructions, then schedule the morning prompt from Section 12.2.

## Which assistants

Claude Projects, Claude Code, Codex, Cursor, and Grok all work if the assistant can read this folder. A browser (for job sites) and email (inbox and sent mail) make the morning run useful. Calendar is optional and should stay read-only unless you ask it to hold a slot.

Point the assistant at `playbook/job-scout-playbook.md` and the files in `profile/`. If chat and a profile file disagree, the playbook says to ask, then update the file.

## Privacy

Filled profiles, resumes, phone numbers, screening answers, digests, drafts, and prep packs stay private. `.gitignore` keeps resumes and run artifacts out of git. Do not commit them to a public fork.

## License

[MIT](LICENSE)

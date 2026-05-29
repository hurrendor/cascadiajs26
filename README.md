# CascadiaJS 2026
In June 2026, the world / Pacific Northwest converged for CascadiaJS 2026. Here are the community notes for conference talks.

## Getting started:
Talk notes are under `talks/`. Everything is in Markdown; no installation needed.

### PR Guidelines:
Community pull requests are encouraged! If you're adding or updating notes, please handle merges with any existing notes.

### Resource links:
- [Conference Schedule](https://cascadiajs.com/2026/schedule)
- [Talks Data Source](https://github.com/cascadiajs/cascadiajs/blob/main/shared/data/2026/talks.json)


### "I just want the templates" or "I want to change the schema":
This repository assumes you already have set up yarn and NodeJS on your computer, and have access to a terminal.
If you'd like to change the schema for next year's talks, or create your own note templates, the notes skeletons are created from `utils/createNoteSkeletons.js`.

From the main directory, run the associated commands in your terminal:
- set up: `yarn install`
- create the note skeletons: `node utils/createNoteSkeletons.js`
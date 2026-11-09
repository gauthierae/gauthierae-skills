# writing-coach

A writing coach as one portable instruction file. It reads your draft and points to weaknesses in three steps: language, reader's path, and implicit meaning. It never rewrites. You write every word.

## The three steps

1. **Language.** Grammar, spelling, usage, interference from your first language, and places where a better word is likely.
2. **Reader's path.** A reverse outline against your aim, drift, off-track sections, gaps for a newcomer, contradictions.
3. **Implicit.** How the coach reads each irony and exaggeration, compared with what you meant.

Each step repeats review and `reread` until you type `next`. The coach works in the language of your draft.

## Install

The whole skill is the file `SKILL.md`.

- **Claude Code or another agent tool that reads `SKILL.md`.** Put the folder in your skills directory (for Claude Code: `~/.claude/skills/writing-coach/`). Call it with the name `writing-coach` and the path of your draft. The coach reads the file at every `reread` and keeps a log next to it.
- **ChatGPT, claude.ai or any chat.** Paste the full text of `SKILL.md` as the first message (or in a custom GPT, project or custom instructions). Then paste your draft. At every `reread`, paste the new version. Type `save` to get the log, and paste it in a new chat to resume.

## Limits

- Tested on Claude only. The `evals/` folder holds the checks. Run them on your model.
- Quotes are exact in file mode (checked with `grep -F`). In chat mode the model checks them by itself, which is weaker.
- The coach is one reader, not your audience. Its reading is a warning, not a verdict.
- Interference tests have detailed patterns for French writers of English. For other language pairs, the model uses its own knowledge.

## License

MIT. See `LICENSE`.

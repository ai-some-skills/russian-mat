# Russian Mat — Матерный русский

**English** | [Русский](README.ru.md)

An Agent Skill for natural Russian profanity (*mat*), expressive colloquial writing, and precise explanations in a rough voice. It lets the user adjust profanity, harshness, and humor independently.

The skill instructions and language references are in Russian. It is designed for Russian speech, including colloquial and euphemistic registers. This English README helps readers discover the skill and understand its controls; the examples stay in Russian because wording and tone matter.

Once the user requests this style, the default is frequent, uncensored profanity. Facts, meaning, links, and technical identifiers are preserved. A request for profanity does not authorize unsolicited personal insults.

## Installation through skills.sh

With Node.js installed, run:

```bash
npx skills add ai-some-skills/russian-mat
```

The CLI offers agent and installation-scope selection. See the [skills.sh documentation](https://skills.sh/docs). The [skills.sh directory](https://skills.sh) uses CLI installation events; publishing a GitHub repository alone does not guarantee immediate listing.

## Installation in Codex

Ask Codex:

```text
Install the skill from https://github.com/ai-some-skills/russian-mat
```

Or copy the repository contents into `~/.codex/skills/russian-mat/`. `SKILL.md` must sit directly in that directory. The skill will be available from the next message after installation.

## Installation in Claude Code

You need Git and an installed copy of Claude Code. To install for all projects:

```bash
git clone https://github.com/ai-some-skills/russian-mat.git \
  ~/.claude/skills/russian-mat
```

If the directory already exists, inspect it first rather than cloning over it. For a single project, use `.claude/skills/russian-mat/` inside that project instead.

In Claude Code, invoke `/russian-mat` or ask **«Общайся со мной матом»** (“Use Russian profanity when talking to me”). The skill follows the Agent Skills format. It requires no additional programs or APIs of its own. See the [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

## Installation in Claude on the web

Skills require code execution to be enabled. Prepare a ZIP with a top-level `russian-mat` directory:

```text
russian-mat.zip
└── russian-mat/
    ├── SKILL.md
    ├── references/
    └── evals/
```

1. Download the repository using **Code → Download ZIP** and extract it.
2. Rename `russian-mat-main` to `russian-mat` and create a new ZIP with the structure above.
3. Open **Customize → Skills → + → Create skill → Upload a skill**, upload the ZIP, and enable the skill.
4. Ask **«Общайся со мной матом»** or specify the tone you want.

Anthropic's instructions: [uploading skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude) and [ZIP structure](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

The structure is prepared for Codex and Claude. Published qualitative trials were run on GPT. The skill has not yet been tested on Claude, so naturalness and retention of tone settings may differ.

## Usage

| Russian request | Meaning and intended scope |
| --- | --- |
| «Общайся со мной матом» | Enable the style for the conversation. |
| «Перепиши этот текст с матом» | Rewrite one text using profanity. |
| «Ещё жёстче» / «помягче» | Make the voice harsher or gentler. |
| «Много мата, но дружелюбно и без шуток» | Use frequent profanity, a friendly tone, and no jokes: three independent settings. |
| «Убавь только мат» / «добавь юмора» | Change one setting without resetting the others. |
| «Перепиши и покажи разбор» | Rewrite and explain the specific edits. |
| «Околоматерно, без прямого мата» | Use euphemisms and hints rather than explicit profanity. |
| «Теперь без мата» / «нейтрально» | Remove profanity; requesting a neutral tone also removes profane hints. |

## Example

**Russian request:** «Много мата, прямо и без шуток. Объясни разницу между аутентификацией и авторизацией».

**English explanation:** The user asks for frequent profanity, a direct tone, no jokes, and an explanation of authentication versus authorization. The rough language emphasizes the distinction without insulting the reader.

**Illustrative response in Russian:**

> Аутентификация проверяет, кто ты. Авторизация — что тебе разрешено.
>
> Вошёл по паролю — заебись, личность подтвердили. Но право удалить чужой проект от этого ни хуя не появилось: для удаления отдельно проверяют права.
>
> «Вошёл» и «можно всё» — разные вещи, блядь. Перепутать их в системе доступа — хуёвая идея.

**Meaning:** Authentication establishes identity; authorization determines permitted actions. Signing in with a password does not itself grant permission to delete someone else's project. The profanity changes the voice, not the technical distinction.

This is an authored illustration of the intended voice, not a result from testing on Claude.

## Contents

The instructions and references linked below are in Russian. Start with the [reference map](references/reference-map.md) to load only the material needed for a task.

- [SKILL.md](SKILL.md): workflow and general constraints.
- [Style controls](references/style-controls.md): profanity, harshness, humor, and scope.
- [Longer conversations](references/conversation-state.md) and [avoiding repetition](references/repetition.md).
- [Lexicon reference](references/lexicon.md): 210 tabular entries across the main vocabulary, extended vocabulary, and expressions.
- [Genres](references/genres.md) and [editorial explanations](references/editing.md).
- [Engineering conversations](references/engineering.md): system states, coordination, and literal instructions.
- [Word formation](references/word-formation.md): new forms and rhyming pairs.
- Speech functions, shades of meaning, collocations, variants, dialogues, and playful techniques: follow the reference map.
- [Single-turn scenarios](evals/evals.json), [longer scenarios](evals/conversations.json), and [qualitative trial results](evals/qualitative-review.md).

## Sources

The skill draws on the dictionary section, proverbs and sayings, and selected folktale, parody, and anecdotal passages from *Русский мат. Антология* (*Russian Mat: An Anthology*), edited by F. N. Ilyasov, 1994. The reference provides brief original paraphrases of selected meanings. The source PDF and full book text are not distributed. Contemporary examples were written for the skill.

Engineering phrasing and rhyming pairs also draw on the public [pohuy](https://github.com/smixs/pohuy) project by Serge Shima (smixs), licensed under MIT. Attribution and the license are preserved in the [third-party notice](third-party/pohuy-LICENSE).

## License

Original instructions, examples, and supporting materials are available under [MIT](LICENSE). The license does not cover the cited book or other third-party works.

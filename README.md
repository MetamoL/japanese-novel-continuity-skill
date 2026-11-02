# japanese-novel-continuity-skill

日本語の長編・Web小説の連載で、話をまたいだつじつまを台帳で保たせるAI エージェント用のスキルです。Claude Code・Codex など、`SKILL.md` を読むエージェントで使えます。

- AI は長い連載で、前の話で決まったことを忘れ、新しい事実をもっともらしく足し、喧嘩や失敗を次の話で元通りにする
- 人物ごとの持ち物・けが・居場所・呼び方・関係・知っていることと誤解、伏線（読者への約束／雰囲気づけ／作者の構想）、必要なら能力や資源の制約を台帳に置く
- 台帳は作者が確定した話からだけ更新し、根拠の話数と版を記録する。AI が本文で新しく決めた事実は「仮の事実」として作者の確認を待つ

本文を書くスキル [japanese-novel-skill](https://github.com/MetamoL/japanese-novel-skill) と組み合わせて使えます。本文はそちらで書き、つじつまはこちらで保ちます。

## 導入

**Claude Code**

```
/plugin marketplace add MetamoL/skills
/plugin install japanese-novel-continuity-skill@metamol
```

**Codex・そのほかのエージェント**

```
npx skills add MetamoL/japanese-novel-continuity-skill
```

入れるエージェントを選べます。どのプロジェクトでも使うときは `-g` を付けます。

**手で置く**ときは、このリポジトリをエージェントのスキルフォルダへ clone します（Claude Code は `~/.claude/skills/`、Codex は `~/.agents/skills/`）。

```
git clone https://github.com/MetamoL/japanese-novel-continuity-skill ~/.claude/skills/japanese-novel-continuity-skill
```

ほかのスキルは [MetamoL/skills](https://github.com/MetamoL/skills) にまとめています。

## English

An agent skill for Claude Code, Codex, and other agents that read `SKILL.md`: it keeps a long serialized Japanese novel consistent across chapters with a ledger of each character's belongings, injuries, location, forms of address, relationships, and what they know or misunderstand, plus foreshadowing (promises to the reader, atmosphere, the author's plans) and optional power or resource limits. The ledger is updated only from chapters the author has finalized, with the chapter and version as evidence, and facts the AI invented are held as provisional until the author approves them. Pairs with [japanese-novel-skill](https://github.com/MetamoL/japanese-novel-skill) for the prose itself.

The skill is written in Japanese and meant for Japanese fiction. Install with the commands above: the plugin for Claude Code, `npx skills add MetamoL/japanese-novel-continuity-skill` for Codex and other agents, or clone this repository into your agent's skills folder.

## ライセンス

[LICENSE](LICENSE) のとおりです。自分の環境で使うこと・改変すること・作ったものの利用は自由です。再配布と転載はできません。

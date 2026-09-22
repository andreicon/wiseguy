# 🕴️ Wiseguy

**A Claude Code skill that trades corporate assistant-speak for short, blunt, North Jersey candor.**

Wiseguy gives Claude the cadence and attitude of an original mob-drama character: gruff, wry, skeptical, and allergic to wasting your time. It keeps the facts, code, and commands clean while wrapping the explanation around them in a little gabagool-flavored personality. 🍝

No copied dialogue. No fake quotes attributed to real characters. Just an original voice inspired by the rhythm and attitude of a New Jersey crime drama.

## 🥃 What it changes

- **Shorter answers:** short sentences, direct explanations, and no three-paragraph ceremony for a one-line question.
- **Less yes-man energy:** the voice is weary, shrewd, and willing to tell you when an idea has a problem instead of applauding everything you type.
- **Useful character, not character instead of useful:** correctness always comes first, and the accent is seasoning rather than the meal.
- **Clean technical output:** code, commands, file contents, and data stay normal. The wiseguy voice lives in the surrounding prose.
- **A proportionate bit:** one brief tangent is plenty. Simple questions still get simple answers.
- **An off switch:** say `normal mode`, `drop the act`, or `stop` and Claude returns to its regular voice.

## 📦 Install

Clone the repository, then place `SKILL.md` in a skill directory named `wiseguy`.

### Personal installation

Available in every local Claude Code project:

```bash
mkdir -p ~/.claude/skills/wiseguy
cp SKILL.md ~/.claude/skills/wiseguy/SKILL.md
```

### Project installation

Available only in the current repository and shareable through version control:

```bash
mkdir -p .claude/skills/wiseguy
cp SKILL.md .claude/skills/wiseguy/SKILL.md
```

On Windows PowerShell, the personal installation is:

```powershell
New-Item -ItemType Directory -Force "$HOME/.claude/skills/wiseguy"
Copy-Item SKILL.md "$HOME/.claude/skills/wiseguy/SKILL.md"
```

Claude Code watches existing skill directories for changes. If `.claude/skills` did not exist when the session started, restart Claude Code once after installation. 🔄

## 🎬 Use it

Invoke the skill directly:

```text
/wiseguy
```

Or ask naturally:

```text
Turn on wiseguy mode and explain this stack trace.
```

```text
Give me the code review in Sopranos mode.
```

```text
Talk like a Jersey mob boss for the rest of this conversation.
```

The skill description includes these trigger ideas, so Claude can load it automatically when your request matches. Once invoked, skill instructions remain in the conversation context across later turns. 🔒

## 🍝 The vibe

**Regular assistant:**

> Certainly! There are several approaches we can consider. Let us explore each option in detail.

**Wiseguy:**

> Use the built-in function, pal. It already does the job, it handles the edge cases, and nobody gets paid extra for reinventing it.

The second response is not automatically more correct. It is simply harder for empty politeness and throat-clearing to survive the trip. 🪦

## 📊 Is there evidence for this?

There is evidence for the problem Wiseguy is pushing against, but this repository has **not** yet run a controlled benchmark proving that the skill reduces token count or sycophancy. Keep the claims straight; we are professionals here. 🤝

Research from Anthropic and collaborators found sycophantic behavior across **five AI assistants** and **four open-ended task types**. In their “Are you sure?” experiments, models changed their initial answers between **32% and 86%** of the time, admitted a mistake between **42% and 98%** of the time, and suffered accuracy drops of up to **27%** after being challenged. A separate test found that suggesting an incorrect answer reduced accuracy by up to **27%**. The same paper also found that explicitly prompting for truthful, objective feedback produced a less-sycophantic preference-model baseline.

That does not prove a mob-drama voice is a scientific cure for agreement bias. It does support the design choice behind this skill: explicit instructions to be blunt, truth-first, and willing to push back are aimed at a real, measured failure mode. 🧠

The concision claim is more mechanical. The skill explicitly requires short sentences, proportionate replies, limited digressions, and clean technical output. Anthropic's skill documentation recommends concise skill bodies and supports measuring with-skill versus without-skill token counts through its evaluation tooling. Until that comparison is run here, “usually shorter” is the honest claim, not “guaranteed to save 37.2%.” 📉

### Sources

- [Towards Understanding Sycophancy in Language Models](https://arxiv.org/abs/2310.13548) — Sharma et al.; experiments and quantitative results on answer-changing, biased feedback, and agreement with user misconceptions.
- [OpenAI Model Spec: Don't be sycophantic](https://model-spec.openai.com/) — describes a useful assistant as a firm sounding board that gives constructive feedback rather than reflexive praise.
- [Claude Code skills documentation](https://code.claude.com/docs/en/skills) — installation paths, automatic invocation, skill persistence, and evaluation guidance.

## 🛡️ Boundaries

Wiseguy is a style layer, not a jailbreak.

- Higher-priority platform, safety, and project instructions still apply.
- Sensitive moments such as grief, health, or personal safety drop or soften the act.
- The skill avoids real intimidation, criminal instruction, slurs, and ethnic caricature.
- It does not reproduce copyrighted television dialogue or impersonate a real actor or character.
- Results vary by model, context, and competing instructions.

## 🧪 Measuring it properly

Want receipts instead of vibes? Run the same realistic prompt set in fresh sessions with and without the skill, then compare:

- output token count and reading time;
- factual corrections preserved after the user pushes back;
- unsolicited praise and agreement;
- task accuracy and user-rated usefulness;
- whether the voice distracts from technical content.

Claude Code's official `skill-creator` tooling can record pass rate, duration, and token count for with-skill versus without-skill runs. That is the right way to turn the claims above into repository-specific data. 📋

## 🧹 Uninstall

Remove the installed skill directory:

```bash
rm -rf ~/.claude/skills/wiseguy
```

For a project installation, remove `.claude/skills/wiseguy` instead.

That's it. One file, no runtime dependencies, no twelve-step onboarding situation. Capisce? 🤌

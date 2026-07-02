# web-verify — Career Intelligence Agent for AI Agent IDEs

**A structured skill for Trae/Cursor/Claude Code that forces the agent to search primary sources, filter marketing noise, and present verified career intelligence — before giving you advice.**

Built for Chinese IT/AI job market. 5 real-world cold-start tests passed.

## What It Does

When you ask "Should I learn LangChain?" or "What's the AI job market like?", a normal agent gives you opinions. With web-verify, the agent:

1. **Searches primary sources first** (BOSS直聘 JD, company earnings reports, Stanford HAI, China Academy of ICT)
2. **Filters out** CSDN career-marketing articles, clickbait success stories, and salary aggregator sites
3. **Runs adversarial verification** — actively searches for contradictory evidence
4. **Labels every source** — [PRIMARY], [CREDIBLE], [UNVERIFIED], or [DISPUTED]
5. **Separates facts from inferences** — tells you what's data and what's analysis

## Install

Copy `SKILL.md` to your IDE's skills directory:

```bash
# Trae IDE
mkdir -p ~/.trae/skills/web-verify
cp SKILL.md ~/.trae/skills/web-verify/

# Cursor
mkdir -p ~/.cursor/skills/web-verify
cp SKILL.md ~/.cursor/skills/web-verify/
```

## Usage

Start any conversation with:

```
Use Skill: web-verify
```

Then ask things like:
- "Java 背景空窗一年转 AI 能找到工作吗？"
- "北京 AI 应用开发薪资多少？"
- "听说 AI 岗位涨了 312%，真的假的？"
- "LangChain 还值得学吗？"

## Verification

5 independent cold-start sessions tested with a new agent (no conversation context). All passed:

| Test | Passed |
|------|:--:|
| Adversarial verification (debunked fake "312%") | ✅ |
| Java-to-AI career transition (found real JD) | ✅ |
| LangChain "learn or skip" with [DISPUTED] tag | ✅ |
| Beijing AI salary from real job postings | ✅ |
| Alibaba/Tencent Q1 earnings analysis | ✅ |

## License

MIT

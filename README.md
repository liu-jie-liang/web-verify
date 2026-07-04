# web-verify — IT/AI 职业情报分析

**让 AI Agent 在回答职业、市场、技术趋势类问题之前，先搜一手信源、过滤营销噪音、标注可信度——再给你结论。**

专为中国 IT/AI 就业市场设计。5 次独立冷启动测试通过。

## 它解决什么问题

你问 Agent "学 LangChain 能找到工作吗？"或"AI 岗位薪资多少？"，普通 Agent 凭训练数据给你观点。加载 web-verify 后，Agent 会：

1. **先搜一手信源**（BOSS直聘 JD、公司财报、Stanford HAI、中国信通院）
2. **过滤营销垃圾**（CSDN 职业类水文、标题党、匿名帖、无源精确数字）
3. **对抗验证** — 主动搜索反面证据，发现矛盾标注 [DISPUTED]
4. **标注每个来源** — [PRIMARY] / [CREDIBLE] / [UNVERIFIED] / [LOW-QUALITY]
5. **区分事实与推断** — 明确告诉你哪部分是数据、哪部分是分析

## 安装

```bash
mkdir -p ~/.trae/skills/web-verify
cp SKILL.md ~/.trae/skills/web-verify/
```

## 使用

```
Use Skill: web-verify
```

然后问你想问的：

- "Java 背景空窗一年转 AI 能找到工作吗？"
- "北京 AI 应用开发薪资多少？"
- "听说 AI 岗位涨了 312%，真的假的？"
- "LangChain 还值得学吗？"

## 已验证

5 次独立冷启动会话测试（全新 Agent，无对话上下文），全部通过：

| 测试场景 | 结果 |
|---------|:--:|
| 对抗验证（拆穿 "AI 岗位涨 312%" 假数据） | ✅ |
| Java 转 AI 职业咨询（找到真实 JD） | ✅ |
| LangChain "学还是不学"（含 [DISPUTED] 标注） | ✅ |
| 北京 AI 应用开发薪资（真实 JD 薪资） | ✅ |
| 阿里/腾讯财报 AI 收入分析 | ✅ |

---
name: project-review
description: >
  Perform a professional, multi-dimensional review of a YouTube video project.
  Use this skill when asked to "review a project", "evaluate scripts", "audit content quality",
  or "give feedback on a video plan". The skill analyzes all standard project files and generates
  a structured review report with scores, strengths, risks, and actionable improvements.
---

# 🎬 Professional YouTube Project Review Skill

## Purpose

This skill enables comprehensive, professional-grade review of any YouTube video project in this repository. It evaluates the project from the perspective of a **full-time YouTube creator and content strategy consultant**, producing a structured review report that identifies strengths, flags risks, and provides actionable improvement suggestions.

## When to Use

Trigger this skill when:
- The user asks to "review", "evaluate", "audit", or "give feedback" on a video project
- The user wants a quality check before production begins
- The user wants to optimize an existing project for better YouTube performance
- The user mentions "评审", "点评", "审查", "优化建议"

## Input Requirements

The review target is a **project folder** following the "One Folder Per Project" structure. The skill expects to find most or all of the following files:

| File | Role in Review |
| :--- | :--- |
| `README.md` | Project planning, logistics, route/budget/gear |
| `script.md` | Main long-form video narrative |
| `short_form_scripts.md` | Short-form content for TikTok/Reels/Stories |
| `shot_list.md` | Camera assignments, shots, and angles |
| `youtube_publish_kit.md` | SEO titles, descriptions, timestamps, hashtags |
| `music/suno_ai_prompts.md` | AI music generation prompts and sound design |
| `thumbnails/ai_cover_prompts.md` | Thumbnail/cover design prompts (if present) |

> [!NOTE]
> Not all files need to exist. The review will cover whatever is available and note any **missing files** as a gap.

## Review Methodology

### Step 1: Read All Project Files

Read every available file in the project folder. Understand the full creative vision, logistics, narrative arc, and distribution strategy.

### Step 2: Score Across 8 Dimensions

Evaluate the project on each dimension using a **1-10 scale**. Provide a brief justification for each score.

| # | Dimension (维度) | What to Evaluate |
| :---: | :--- | :--- |
| 1 | **叙事结构 (Narrative Arc)** | Story structure (3-act, hero's journey, etc.), emotional progression, pacing, narrative tension |
| 2 | **视觉策略 (Visual Strategy)** | Camera assignments, multi-device coordination, shot variety, visual storytelling, color/tone design |
| 3 | **观众留存设计 (Retention Design)** | Hook effectiveness (first 30s), mid-video retention anchors, "5-minute death zone" mitigation, audience interaction prompts |
| 4 | **SEO 与分发 (SEO & Distribution)** | Title strategy, keyword density, multilingual SEO, description optimization, hashtag strategy, end screen/card planning |
| 5 | **短视频矩阵 (Short-form Matrix)** | Content type diversity, platform-specific adaptation, release timeline, viral potential, controversial/opinion-type content |
| 6 | **音乐与声音设计 (Audio Design)** | BGM-emotion alignment using YouTube Audio Library genre/mood taxonomy (see below), SFX design, transition sounds, signature sounds, Suno prompt quality, BPM specifications |
| 7 | **商业可行性 (Monetization)** | Sponsor integration naturalness, ad placement timing, monetization diversity, brand safety |
| 8 | **后勤与可执行性 (Logistics)** | Planning completeness, risk management, contingency plans, budget realism, gear readiness |

### Step 3: Identify Key Strengths (核心亮点)

Highlight **2-4 standout strengths** with detailed explanations of why they work. Reference specific lines or sections from the project files. Use the format:

```markdown
### 🏆 [Strength Title]
[Detailed explanation with specific references]
```

### Step 4: Flag Critical Risks (关键风险)

Identify **3-6 critical risks** ranked by impact. For each risk:
1. **Name the problem** clearly
2. **Explain why it matters** (with YouTube data/behavioral insights)
3. **Provide a concrete solution** with example text/structure

Use this format:

```markdown
### 风险 N：[Risk Title]

**问题**：[Problem description with context]

**解决方案**：[Specific, actionable fix with examples]
```

Focus especially on these high-impact areas:
- **Hook weakness** — Does the first 30 seconds create an "unskippable" promise?
- **Mid-video retention** — Is there a "5-minute death zone" with no tension/stakes?
- **SEO gaps** — Missing multilingual optimization? Weak title strategy?
- **Missing content types** — No controversial/opinion-based short-form content?
- **Sponsor placement** — Integration too long or in low-attention segments?

### Step 5: Generate Action Items (行动清单)

Produce a prioritized table of improvements:

| Priority | Action | Affected Files |
| :---: | :--- | :--- |
| 🔴 P0 | [Must-fix before production] | `file.md` |
| 🟡 P1 | [Should-fix, high impact] | `file.md` |
| 🟢 P2 | [Nice-to-have polish] | `file.md` |

### Step 6: Per-File Detailed Review (逐文件点评)

For **each file** that exists in the project, provide:
- **优点 (Strengths)**: 2-3 specific things done well
- **不足 (Weaknesses)**: 2-3 specific gaps with suggested fixes (include example markdown/text when helpful)

### Step 7: Bonus Creative Ideas (创意加分建议)

Suggest **2-4 creative ideas** that go beyond fixing problems — ideas that could elevate the project to the next level. These should feel inspiring and unexpected.

## Output Format

Generate the review as a markdown file saved to `review/professional_review.md` inside the project folder. Use the following structure:

```markdown
# 🎬 专业脚本评审报告 (Professional Script Review)

> **项目**：[Project Name]
> **评审视角**：YouTube 全职创作者 / 内容策略顾问
> **评审日期**：[Date]
> **评审范围**：[List of files reviewed]

---

## 📊 总体评分 (Overall Score)

[Scoring table across 8 dimensions + weighted overall score]

---

## ✅ 核心亮点 (Key Strengths)

[2-4 detailed strengths]

---

## ⚠️ 关键风险与改进建议 (Critical Improvements)

[3-6 risks with problems and solutions]

---

## 🎯 高优先级行动清单 (Action Items)

[Prioritized action table]

---

## 🔬 逐文件详细点评

[Per-file strengths and weaknesses]

---

## 💡 创意加分建议 (Bonus Ideas)

[2-4 creative enhancement ideas]

---

## 🎯 结论

[Summary assessment with the 1-2 most critical improvements]
```

## Review Principles

1. **Be specific, not generic** — Reference exact VO lines, shot descriptions, or timestamps when giving feedback. Vague advice is useless.
2. **Data-informed** — Ground retention and SEO advice in real YouTube analytics patterns (e.g., "front 30s retention determines algorithmic push", "5-8 min is the typical drop-off zone for 15-20 min videos").
3. **Actionable over theoretical** — Every piece of criticism must include a concrete fix with example text or structure.
4. **Respect the creator's voice** — Don't suggest changes that fundamentally alter the creator's style or vision. Enhance, don't replace.
5. **Bilingual awareness** — This channel targets both Chinese and English-speaking audiences. Review SEO and titles for both markets.
6. **Gear-aware** — Reference the production stack (DJI Pocket 3, Insta360 Ace Pro 2, DJI Mavic 4 Pro, Leica M11-P, Kawasaki W175) when suggesting shots or visual improvements.
7. **Cross-platform thinking** — Always consider both long-form (YouTube) and short-form (TikTok/Reels) implications of any suggestion.

## YouTube Audio Library: Standard Genre & Mood Reference

When reviewing or generating music design, always use the official **YouTube Audio Library** taxonomy to classify background music. This ensures compatibility with YouTube's own library and provides clear, standardized communication with editors and collaborators.

### 🎼 Genres（流派）

| Genre (EN) | 流派（中文） |
| :--- | :--- |
| Alternative & Punk | 另类和朋克 |
| Ambient | 氛围音乐 |
| Children's | 儿童 |
| Cinematic | 电影 |
| Classical | 古典乐 |
| Country & Folk | 乡村音乐和民谣 |
| Dance & Electronic | 舞蹈和电子音乐 |
| Hip-Hop & Rap | 嘻哈饶舌说唱 |
| Holiday | 假日音乐 |
| Jazz & Blues | 爵士与布鲁斯 |
| Pop | 流行乐 |
| R&B & Soul | R&B 和灵魂乐 |
| Reggae | 雷鬼乐 |
| Rock | 摇滚乐 |

### 🎭 Moods（曲调）

| Mood (EN) | 曲调（中文） |
| :--- | :--- |
| Angry | 愤怒 |
| Bright | 欢快 |
| Calm | 平静 |
| Dark | 忧郁 |
| Dramatic | 激越 |
| Funky | 放克 |
| Happy | 欢快 |
| Inspirational | 励志 |
| Romantic | 浪漫 |
| Sad | 悲伤 |

> [!TIP]
> When evaluating `music/suno_ai_prompts.md`, check that each section explicitly maps to one of the above official genres and moods. Mismatches between the intended emotional arc and the chosen genre/mood are a common quality issue.

---

## Contextual References

When reviewing, consider checking:
- `/Sponsors/` directory for brand voice and key talking points
- `/Templates/` for any established project templates
- Other completed projects in the same category for consistency patterns
- `GEMINI.md` at the repository root for overall project context

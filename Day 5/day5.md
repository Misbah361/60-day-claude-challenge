# Day 5: Context Engineering

## Task
Compare two versions of the same prompt — one generic (no context) and one context-rich (with learner details) — and observe how the outputs differ.

## Prompt A (No Context)
```
Create a 30-day learning roadmap.

Include:
- Weekly milestones
- Daily tasks
- Resources
- Projects
- Final outcome

Make it practical and beginner-friendly.
```

**What happened:** Claude couldn't proceed straight away — it had to stop and ask *"What topic should this roadmap cover?"* I left it as "No preference," and Claude defaulted to an **AI/ML fundamentals roadmap**, assuming a beginner starting from zero.

📄 Output: `30-Day-AI-ML-Roadmap.md`

## Prompt B (With Context)
```
Create a 30-day learning roadmap.

Context:
- Current Situation: [Student]
- Current Skills: [Python]
- Goal: [Learn Coding]
- Available Time: [1 hour per day]
- Experience Level: [Beginner]
- Preferred Learning Style: [Videos, Projects and Reading]

Include:
- Weekly milestones
- Daily tasks
- Resources
- Projects
- Final outcome

Make it practical and beginner-friendly.
```

**What happened:** Claude generated the roadmap immediately — no clarifying question needed. It also caught a nuance I hadn't explicitly stated: since I already knew Python, it built an **intermediate Python + fundamentals roadmap** instead of a from-scratch beginner one, explicitly noting *"since you already know Python, I'll build this as an intermediate Python roadmap."*

📄 Output: `30-Day-Intermediate-Python-Roadmap.md`

## Key Learnings

1. **Context removes ambiguity, not just adds detail.** Prompt A had to pause and ask what topic I even wanted. Prompt B skipped that entirely because the context already answered the implicit questions.

2. **Context changes the *substance* of the output, not just the tone.** Both prompts asked for a "beginner-friendly" roadmap — but Prompt B correctly overrode "beginner" with "intermediate" once it saw I already knew Python. Context can catch nuance that even the instructions themselves get technically wrong.

3. **Without context, the AI guesses — and its guess may not match your actual need.** Prompt A defaulted to a broad AI/ML roadmap that had nothing to do with what I actually needed next (leveling up my Python). A well-guessed generic answer is still a mismatched answer.

4. **Structure and pacing shift with context too.** Prompt B's roadmap explicitly matched my "1 hour/day" pace and "videos + projects + reading" style in its resource choices (Corey Schafer/CS Dojo videos, hands-on weekend projects). Prompt A had no such personalization to work with.

5. **Takeaway:** Good prompting tells the AI *what to do*. Good context engineering tells the AI *who it's doing it for* — and that second part often matters more for getting a genuinely useful output on the first try.

# Day 2/60 — Prompt Engineering: Lazy vs. Engineered

## What I Worked On
Today's focus was understanding prompt engineering in practice, not just in theory. I ran the same idea through Claude twice — once as a rough, unstructured prompt, and once after optimizing it with the MetaPrompt Chrome extension — then compared the results.

## The Prompts

**Lazy prompt:**
> "Create an image explaining Prompt Engineering."

**Engineered prompt (via MetaPrompt):**
A structured, detailed version of the same request — specifying format (infographic), audience, and design constraints instead of leaving them to guesswork.

## What I Noticed

**Explanation quality:** The lazy prompt gave a solid conceptual overview — five core ideas (Clear task, Context, Examples, Output format, Constraints) in an interactive diagram. The engineered prompt went further, including a real before/after example so the concept was demonstrated, not just described.

**Structure:** The lazy output was a flat set of boxes leading to one conclusion. The engineered output had real document structure — numbered sections, a flow diagram, an 8-step vague-to-precise transformation guide, and a dedicated design-spec section.

**Examples:** The lazy version used abstract labels ("show, don't just tell"). The engineered version included a concrete before/after prompt pair (a birthday party planning example), spelled out in full — instantly clearer than an abstract label.

**Output usability:** The lazy prompt produced a diagram viewable only in that chat. The engineered prompt produced a downloadable HTML file with a defined color palette and exact pixel dimensions for social media and print — a ready-to-use asset, not just a visual.

## Key Takeaway
Specificity compounds. Giving Claude context — audience, format, constraints — didn't just make the explanation better, it changed the *category* of output entirely: from a quick summary to a usable deliverable. Prompt engineering isn't about phrasing things "nicely" — it's about front-loading the decisions the model would otherwise have to guess at.

## Files in This Folder
- `lazy-prompt-result.png` — screenshot of the unstructured prompt's output
- `engineered-prompt-result.png` — screenshot of the MetaPrompt-optimized prompt's output
- `prompt_engineering_infographic.html` — the full interactive infographic generated from the engineered prompt (open in browser to view/export)

## Tool Used
[MetaPrompt](https://chromewebstore.google.com/detail/metaprompt-ai-prompt-engi/glkfhecdpcmaclfkhkibmoijipnnjkbf) — Chrome extension for rewriting rough prompts into structured ones before sending to Claude.

# Day 13 — AI-Powered Job Search & Skill-Gap Analysis

## Objective
Use Claude connected to the Indeed MCP connector to build a professional profile, define job search criteria, and discover + analyze real AI/ML, Data Science, and Python Developer internship opportunities matching my background.

## Workflow

**Prompt 1 — Professional Profile**
Gave Claude my academic background, skills (Python, NumPy, pandas, Matplotlib, Flask, SQL, JS, React, TypeScript, TailwindCSS, Git), and project experience (Circuit.IQ, NutriScope, Environmental Health Analyzer) to generate a structured professional profile.

**Prompt 2 — Job Search Criteria**
Defined target roles (AI/ML Intern, Data Science Intern, Python Developer Intern), remote/hybrid preference, startup/mid-size company focus prioritizing mentorship over brand or pay, and a 30-day posting recency window.

**Prompt 3 — Job Discovery & Analysis**
Connected the Indeed MCP connector and had Claude search live listings against my criteria, score them for fit, and run a skill-gap + market-demand analysis.

## Discovered Opportunities (Top Matches)

| Company | Role | Location | Match Score |
|---|---|---|---|
| Pixxel | AI & Data Engineering Intern | Bengaluru | 8/10 |
| Optimspace | Data Science Intern | Remote | 7/10 |
| DataFoundry | AI ML Intern | Remote | 7/10 |
| Portcast | Data Analyst Intern | Remote | 6.5/10 |
| Quadrantech | AI/ML Intern | Hyderabad | 6/10 |
| FDM Digital Solutions | AI/ML Intern | Gurugram | 6/10 |
| MNJ Software | Data Science Intern | Remote | 5.5/10 |

🚩 None of the listings returned CTC/compensation data via the connector — flagged rather than estimated.

## Skill-Gap Analysis
- **scikit-learn / applied ML modeling** — biggest gap; implied in nearly every AI/ML-titled posting
- **Formal statistics** — often assumed for Data Science-titled roles
- **Cloud/deployment exposure** — expected for data-engineering-leaning roles
- **FastAPI** — increasingly preferred over Flask for ML-serving APIs in newer postings

## Market Demand Insights
- True remote AI/ML internships are less common than remote Data Science/Data Analyst titles; pure AI/ML roles skew onsite (Bengaluru, Hyderabad, Delhi NCR)
- Many listings labeled "internship" are actually fresher/full-time roles — title filtering alone isn't reliable; manual JD review is necessary
- Startups outside the obvious "AI/ML" label (space-tech, logistics-tech) are actively hiring for data/Python skillsets

## Key Learnings
1. Real job-market data exposes a sharper, more specific skill gap than a resume audit alone — scikit-learn keeps surfacing as the single highest-leverage skill to add next.
2. Internship title labels on job boards are inconsistent; "AI/ML Intern" sometimes means full-stack work, and "internship" sometimes means fresher/full-time. Always verify against the JD body.
3. Compensation transparency is low at the internship level — plan to ask directly during outreach rather than relying on listings.
4. Connecting a live job-data source (vs. static resume review) turns skill-gap analysis from generic advice into something tied to actual postings I could apply to today.

## Next Steps
- Build one applied ML project using scikit-learn to directly close the top-cited gap
- Apply to the highest-fit roles (Pixxel, Optimspace, DataFoundry) leading with the Circuit.IQ project
- Ask about hybrid/remote flexibility for onsite-only roles before ruling them out

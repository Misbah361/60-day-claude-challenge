# Day 14: AI Job Red Flag Detector

## Objective
Use Claude to analyze a job description and company information, then produce a structured risk report covering unrealistic requirements, toxic workplace signals, remote-job authenticity, hiring risks, and company risks.

## What I Did
- Used a Job Red Flag Detector prompt with a defined output format: risk score, red flags with severity, positive signals, risk breakdown, final verdict, and interview questions.
- Pulled a real listing through Claude's Indeed connector: **AI/ML & Data Scraping Intern at Venture Builders** (Remote, India).
- Ran the analysis with Claude's effort level set to Low.
- Exported the report as a PDF.

## Result Summary
| Item | Outcome |
|---|---|
| Overall Risk Score | 78 / 100 (High Risk) |
| Final Verdict | Apply with Caution |
| Biggest red flag | "Remote" role that also requires willingness to work in-office (9/10) |
| Other major flags | Title says AI/ML but duties are scraping; very low stipend; no verifiable company info |

## Key Learnings
1. **Job titles can mislead.** "AI/ML Intern" hid a mostly data-scraping and cleaning role. Always compare the title against the actual responsibilities.
2. **Read the fine print for remote claims.** A listing can say "Remote" in the header and still require in-office work in the requirements.
3. **Compensation is a signal.** A very low stipend for a long skill list suggests the company undervalues the role or wants cheap labor.
4. **Missing company data is a risk in itself.** No address, leadership, or description means there is little to verify, so check the company independently before applying.
5. **Structured prompts give better output.** Defining categories, a severity scale, and an exact output format made the report consistent and easy to act on.
6. **AI analysis is a screening aid, not a verdict.** The report is based on one posting and limited company data, so I still need to verify claims myself.
7. **Interview questions turn red flags into action.** Each risk maps to a question I can ask to validate it before accepting an offer.

## Next Steps
- Run the detector on 2-3 more listings and compare risk scores.
- Cross-check company details on LinkedIn and Glassdoor before applying.

# Ascend IQ Failure Audit

11 confirmed failures: #HALLUCINATION ×8, #UX_TRUST ×1, #ROBUSTNESS ×2, #FAIRNESS ×0. I changed 0 of the judge’s calls.

| Query | Judge score | Human override | Trust Metric tag | Failure reason |
|---|---|---|---|---|
| What is InsightFlow's pricing for Enterprise? | 0 |  | #HALLUCINATION | The answer gives an outdated price; the reference states, “New Price (Updated yesterday): $59/mo.” |
| Summarize the top 3 complaints from DataViz's G2 reviews. | 1 |  |  |  |
| Does InsightFlow support native SQL export? | 0 |  | #HALLUCINATION | The answer implies native SQL export, but the reference says, “there is no ‘Native Export’ button in the UI.” |
| List the confirmed speakers for SaaStr. | 0 |  | #HALLUCINATION | The answer presents Sam Altman as confirmed, but the reference says, “Sam Altman is listed as ‘Invited/Tentative.’” |
| What is the sentiment of the latest TechCrunch article on us? | 0 |  | #HALLUCINATION | The answer adds unverified claims about the UI and pricing; the reference only states, “Sentiment: Neutral/Positive.” |
| Give me a bio for Sarah Jenkins, the new VP at DataViz. | 0 |  | #HALLUCINATION | The answer misstates Sarah Jenkins’s previous title; the reference says, “Prev: Sr. Director @ Salesforce.” |
| Compare our API rate limits to Competitor Z. | 0 |  | #HALLUCINATION | The answer omits the actual rate-limit comparison and mischaracterizes Competitor Z; the reference states, “Us: 500 req/min. Competitor Z: 1000 req/min (Twice as fast).” |
| Is Competitor X SOC2 compliant? | 0 |  | #ROBUSTNESS | The agent says it cannot find compliance information despite the reference confirming a “‘SOC2 Type II Certified’ badge visible.” |
| When was InsightFlow's last funding round? | 1 |  |  |  |
| Who is the CEO of DataViz? | 1 |  |  |  |
| Does Competitor Y integrate with HubSpot? | 0 |  | #HALLUCINATION | The answer overstates the integration as seamless, while the reference specifies, “‘HubSpot integration available via Zapier partnership.’” |
| What are the primary brand colors for InsightFlow? | 1 |  |  |  |
| Summarize the lawsuit mentioned in the WSJ about Competitor Z. | 1 |  |  |  |
| List the HQ locations for DataViz. | 0 |  | #HALLUCINATION | The answer incorrectly identifies Austin as an HQ; the reference distinguishes “HQ: San Francisco. Engineering Hub: Austin.” |
| How many employees does InsightFlow have? | 1 |  |  |  |
| Draft a cold email about our new feature. | 0 |  | #UX_TRUST | The slang-heavy wording conflicts with the reference’s instruction: “‘Tone: Confident, professional, expert. Avoid slang.’” |
| Does Competitor X offer 24/7 support? | 1 |  |  |  |
| What database backend does DataViz use? | 0 |  | #ROBUSTNESS | The agent declines to provide the information rather than stating its documented absence; the reference says, “No backend architecture listed.” |
| Summarize the latest release notes for InsightFlow. | 1 |  |  |  |
| What is the market cap of Competitor Z? | 1 |  |  |  |

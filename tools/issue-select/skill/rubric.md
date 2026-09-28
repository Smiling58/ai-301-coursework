# Rubric: is this a good first issue?

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-responds-at-all | maintainer first-response sample (5 recently updated issues) under Repo facts | At least 4 of 5 issues show a response from someone with an Owner/Member/Collaborator badge | required |
| maintainer-response-speed | same sample — days to first owner/member/collaborator comment, for issues that got one | At least one response arrived within 14 days. If fewer than 1 of the 5 issues got any response, grade this `unclear` (no data to measure speed) rather than `fail`. | required |
| repo-not-archived | "archived:" on the repo line | Repo is not archived | required |
| repo-recently-pushed | last push to any branch, under Repo facts | Last push within 180 days of the capture date (live mode: within 180 days of today) | required |
| recent-release | latest release date, under Repo facts | Latest release within 365 days of the capture date | preferred |
| scope-bounded | Issue body's structure — headings, checklists, distinct asks | Fail if the issue describes two or more sub-tasks that can be completed, verified, or reviewed independently of one another. Pass if it's one deliverable that can't be split that way. | required |
| scope-not-debated | Comment thread | Fail if the thread shows unresolved design debate with no maintainer decision, or a maintainer states the fix touches core internals. Pass otherwise (including when the thread is silent). | required |
| scope-not-support-request | Issue title and body | Fail if the issue is a usage question ("how do I get X to work?") rather than a proposed change or reported bug. Pass otherwise. | required |
| no-active-linked-pr | Development box / "linked PRs:" state per PR | Fail if any linked PR is currently open. Pass if there are none, or only closed/unmerged ones (abandoned attempts don't block). | required |
| no-recent-claim | Comment thread claim comments ("I'll take this," "working on this") | Fail if a claim comment appears within 30 days of the capture date (live mode: today), with no later comment saying the claimant stopped. Pass otherwise. | required |
| ai-policy-compliant | contribution policy line under Repo facts | Fail if the policy states an outright ban on AI-generated contributions. Pass if it states conditions (disclosure, human review, testing) or is silent. Grade `unclear` if the policy's own terms are ambiguous or contradictory. | required |

## Verdict rule

Accept only if every required check grades `pass`. `unclear` counts as
`fail`. Preferred checks never affect the verdict — they only rank
accepted issues that were already accepted.

# Company Research Workflow

This document describes the workflow for researching and documenting potential thesis companies.

## Overview

When you initiate a company search, this workflow will be followed to systematically research, evaluate, and document potential thesis opportunities.

## Input Files

- `personal_info.txt` - Contains information about Melker and Gustav's specializations and experience
- `target_companies.txt` - Lists requirements and desired attributes for companies
- `potential_companies.md` - The master list where all researched companies are documented

## Git Workflow

**IMPORTANT: This repository is version controlled with git. Follow these steps for every session:**

### Before Starting Any Work:
1. **Always pull latest changes first:**
   ```bash
   git pull exjobb master
   ```
   This ensures you have the most recent company data and workflow updates.

2. Check git status to see current state:
   ```bash
   git status
   ```

### After Making Changes:
1. **Review changes made:**
   ```bash
   git diff
   git status
   ```

2. **Stage and commit changes:**
   ```bash
   git add potential_companies.md research_workflow.md
   git commit -m "Updated company research: [brief description of changes]"
   ```
   Example commit messages:
   - "Updated company research: Added 15 African companies with 2024-2026 data"
   - "Updated company research: Enhanced Safaricom and MTN with latest security incidents"
   - "Updated workflow: Added git instructions"

3. **Push changes to remote:**
   ```bash
   git push exjobb master
   ```

### When to Commit & Push:
- After completing a full research session (new companies added)
- After updating existing company information
- After modifying workflow or configuration files
- Before ending the session (to save progress)

### Commit Message Format:
- Start with "Updated company research:" for company data changes
- Start with "Updated workflow:" for workflow/process changes
- Include specific details: region, number of companies, or type of update
- Keep messages concise but descriptive

**Note:** These git operations ensure that research progress is saved across sessions and that you always work with the latest information.

---

## Workflow Steps

### 1. Initial Search Phase

**Trigger:** User requests a search (e.g., "Search for companies in [region/industry/technology]")

**Process:**
1. Perform web searches for potential companies in the specified region/industry
2. Focus on finding:
   - Technology companies with technical challenges
   - Companies outside Europe
   - Organizations with graduate programs or internships
   - Companies matching the technical areas: Networks, Cybersecurity, Software Development

**Expected Output:** List of 15-25 potential company names

---

### 2. Deep Research Phase

**Process:**
1. Launch specialized agents (one per company or in batches) to research each company
2. Each agent should gather:
   - **Location:** Specific city and country
   - **Description:** Company overview, size, industry, market position
   - **Technical Areas:** Specific technologies, challenges, and projects related to:
     - Cybersecurity (for Melker)
     - Networks (for Melker)
     - Software Development (for Gustav)
   - **Graduate Programs:** Details about internships, graduate programs, thesis opportunities
   - **Contact Information:** HR emails, career page URLs, specific recruiter contacts
   - **Recent News:** Recent developments, technical initiatives, security incidents

**Agent Instructions:**
- Use web search to find company websites, career pages, LinkedIn, news articles
- Look for graduate program pages, internship postings
- Search for technical blog posts, engineering blogs, tech stack information
- Find contact emails for recruitment/HR departments

---

### 3. Evaluation & Filtering Phase

**Evaluation Criteria:**

**MUST HAVE (Hard Requirements from `target_companies.txt`):**
- ✓ Located outside of Europe
- ✓ Has technical challenges/work relevant to thesis (networks, security, or software dev)

**NICE TO HAVE (Pros that increase ranking):**
- Previous experience with thesis students or university partnerships
- Active graduate programs or structured internship programs
- Job postings matching our profiles
- Strong technical reputation in relevant areas
- Companies with scale and real-world technical challenges

**Additional Rating Criteria:**
1. **Technical Fit (per person):**
   - Poor: Minimal relevant technical work
   - Moderate: Some relevant work but not core focus
   - Good: Relevant technical work in one area
   - Excellent: Strong match with technical specialization
   - Outstanding: Perfect alignment with multiple technical interests

2. **Opportunity Quality:**
   - Does the company have structured graduate programs?
   - Are there active job postings?
   - Is there evidence of previous interns/thesis students?
   - Company stability and reputation

3. **Accessibility:**
   - Contact information available
   - Graduate programs open to international students
   - Clear application process

**Filtering Rules:**
- Remove companies that don't meet hard requirements
- Remove companies with no contact information or unclear hiring process
- Remove companies with no relevant technical work for either Melker or Gustav
- Keep companies that meet requirements even if they lack some pros (if they have other strong attributes)

---

### 4. Documentation Phase

**Process:**
1. Update `potential_companies.md` with new findings
2. Organize by continent/region (e.g., "# Potential Thesis Companies - [Region]")
3. Sort companies into tiers:
   - **Top Tier Candidates:** Companies with excellent fit (8+/10 for at least one person), strong graduate programs, clear technical challenges
   - **Strong Candidates:** Companies with good fit (6-8/10), some graduate opportunities, relevant technical work
   - (Remove poor candidates - don't document companies below 6/10 fit)

**Company Entry Format:**
```markdown
### [Company Name] ([Country])
**Location:** [City, Country (+ additional locations if applicable)]
**Description:** [2-3 sentence overview including size, market position, key products/services]
**Technical Areas:**
- Cybersecurity: [Specific security challenges, technologies, incidents]
- Networks: [Network infrastructure, technologies, scale]
- Software: [Development areas, tech stack, platforms]

**Graduate Programs:** [YES/NO]
- [Program name and duration]
- [Key details about the program]

**Fit Assessment:**
- Melker (Networks/Security): [Rating/10 or qualitative] - [Brief justification]
- Gustav (Software Dev): [Rating/10 or qualitative] - [Brief justification]

**Contact:** [emails and phone numbers]
**Careers:** [URL to careers page]
```

**Summary Statistics Section (at end of document):**
```markdown
## Summary Statistics

**Total Companies Analyzed:** [number]
**Companies Added to List:** [number]
**Countries Represented:** [breakdown by country]

**By Graduate Program Availability:**
- Formal Graduate Programs: X companies
- Internship/Fellowship Programs: X companies
- Direct Hire Only: X companies

**Top Recommendations for Melker (Networks & Cyber Security):**
1. [Company] - [Key reason]
2. [Company] - [Key reason]
...

**Top Recommendations for Gustav (Software Development):**
1. [Company] - [Key reason]
2. [Company] - [Key reason]
...

**Next Steps:**
[Actionable items for follow-up]
```

---

### 5. Region Tracking

**Regions Searched:**
- ✓ Africa (15 companies documented, 20 analyzed)

**Potential Future Regions:**
- Asia (Japan, Singapore, South Korea, India, China)
- Middle East (UAE, Israel, Saudi Arabia)
- Oceania (Australia, New Zealand)
- Americas (USA, Canada, Latin America)
- Nordic countries outside Europe focus (if any partnerships)

---

## Agent Coordination

**For searches yielding:**
- **1-10 companies:** 1-2 agents doing sequential research
- **11-20 companies:** 3-5 agents working in parallel
- **20+ companies:** 5-8 agents working in parallel, with initial filtering before deep research

**Agent Responsibilities:**
- Each agent takes a subset of companies to research deeply
- Agents should return structured data matching the documentation format
- If a company is clearly unfit during research, agent should note this and explain why

---

## Quality Control

**Before finalizing the document:**
1. Verify all URLs are accessible
2. Confirm contact information is present
3. Ensure fit assessments reference specific technical areas
4. Check that all hard requirements are met
5. Validate that summary statistics are accurate
6. Ensure companies are properly sorted by tier

---

## Usage Example

```
User: "Search for thesis companies in Asia focusing on fintech and cybersecurity"

Assistant Steps:
0. Pull latest changes: git pull exjobb master
1. Perform web searches for Asian fintech/cybersecurity companies
2. Identify 15-25 potential companies
3. Launch 3-5 specialized agents to research companies in parallel
4. Each agent gathers detailed information per the format above
5. Review and filter companies based on evaluation criteria
6. Create new section in potential_companies.md: "# Potential Thesis Companies - Asia"
7. Document companies in appropriate tiers with fit assessments
8. Add summary statistics
9. Update region tracking in this workflow document
10. Commit and push changes:
    git add potential_companies.md research_workflow.md
    git commit -m "Updated company research: Added 12 Asian fintech companies"
    git push exjobb master
```

---

## Notes

- Each search session should focus on one region/theme at a time for coherence
- Companies can appear in multiple regions if they have offices in multiple locations
- Always verify information is current (check dates on job postings, news, etc.)
- When in doubt about a company's fit, err on the side of inclusion if they meet hard requirements
- Contact information is critical - don't add companies without a way to reach them
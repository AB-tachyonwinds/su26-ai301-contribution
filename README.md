# Contribution [1]: Contact Form Submission - Suggestion (Problem Solution - 2007 - Pairs (ID: ioi-07-pairs))

**Contribution Number:** [1]  
**Student:** Angelie Bautista  
**Issue:** [\[GitHub issue link\] ](https://github.com/cpinitiative/usaco-guide/issues/5867)  
**Status:** [Phase II] [In Progress]

---

## Why I Chose This Issue

I chose issue 5867 "Contact Form Submission - Suggestion (Problem Solution - 2007 - Pairs (ID: ioi-07-pairs))", due to my familiarity with Javascript and Typescript. I believe I can learn MDX within a reasonable time and contributing to this project will widen my tech skills for websites. The issue is marked as a good first issue and the maintainer is active. Additionally, my job goals align with USACO's mission to support computing education for high schoolers through competitions and well-documented guides. I hope to understand how USACO organizes their learning material and communicates with each other in order to apply it to my future endeavors.

The issue is a suggestion to move 2007 - Pairs into the Prefix Sum section. In the issue thread, the maintainer agreed to the change. Ultimately, my contribution will improve topic organization for 2007 - Pairs.

---

## Understanding the Issue

### Problem Description

"Pairs" from the 2007 problem set could appear in a Silver module on Prefix Sums or a related Prefix Sum module with the user's solution. This change is classified as an enhancement for the site.


### Expected Behavior

The "Pairs" problem would appear in a problem list for "More on Prefix Sums", as it applies 2D prefix sums. Alternatively, it can appear in a Platinum section related to prefix sums.

### Current Behavior

"Pairs" is currently only directly referenced to a Platinum module on 2D Range Queries, as seen at the top of the user solution page (https://usaco.guide/problems/ioi-07-pairs/user-solutions).

### Affected Components

Relevant components fo are located inside the /content directory. The most relevant module .mdx file would be 3_Silver/More_Prefix_Sums.mdx.

---

## Reproduction Process

### Environment Setup

USACO Guide supports an online live editor, but I chose to test the site locally using Yarn as written in the Contribution Guide. Had it running in 20 minutes and my only issue was admin access for corepack enable, which is a required tool for managing package managers like Yarn.

Working branch: https://github.com/AB-tachyonwinds/usaco-guide

### Steps to Reproduce
View the most relevant existing module for Prefix Sums:
1. Navigate to http://localhost:3000/silver/more-prefix-sums
2. Scroll down to Problems section after Solution for Forest Queries 
3. Pairs could potentially be added to that table as a Hard (or Very Hard) question

### Reproduction Evidence

Branch:
https://github.com/AB-tachyonwinds/usaco-guide/tree/fix-issue-5867
- **Screenshots/logs:** ![topview](images/usersolutions-topview.png)
Current text signifying modules referencing the Pairs problem. We want Prefix Sum to appear here.
![problem list](images/more-prefix-sum-problemlist.png)
Current problem list of More Prefix Sums in Silver
- **My findings:** A module is largely made up of its mdx file and a corresponding json file specifically for the problem list.

---

## Solution Approach

### Analysis

To add problems to the More Prefix Sums module, we must edit the More_Prefix_Sums.problems.json file.

### Proposed Solution

Inside the "cum2" section of More_Prefix_Sums.problems.json, we must add an entry that includes uniqueId, name, url, source, difficulty, isStarred, tags, and solution metadata. Because a uniqueId already exists for Pairs due to be mentioned in 2D Range Queries, we will reference the uniqueId from 2DRQ.problems.json.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** The 2007 problem "Pairs" can be added to the Prefix Sums section. The More on Prefix Sums is the most appropriate existing module due to the submitter's proposed solution using 2D prefix sum.

**Match:** Other modules have a similar mdx and json structure that we can reference.

**Plan:** 
1. Modify More_Prefix_Sums.problems.json and match the format to add Pairs to cum2 (problem list ID representing cumulative sums for 2D).
2. Run the site locally to check for changes in http://localhost:3000/silver/more-prefix-sums and http://localhost:3000/problems/ioi-07-pairs/user-solutions

**Implement:** https://github.com/AB-tachyonwinds/usaco-guide/tree/fix-issue-5867

**Review:** Will review the Contributing module (includes Contributing, Adding Solutions, Introducing Modules, and working with MDX)

**Evaluate:** Will run the site locally through Yarn and check all sections that reference Pairs for intended behavior.

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]

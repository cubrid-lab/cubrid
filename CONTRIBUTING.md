First off, thank you for considering contributing to CUBRID. 

There are many ways to contribute, from submitting a bug report and a feature request, improving the documentation, sharing sample codes, writing a blog or issuing a patch.

## GitHub issues and change descriptions within cubrid-lab

For GitHub issues maintained in this repository, give every title a type-only prefix: `feat:`, `bug:`, `docs:`, `test:`, `chore:` or `ci:` (no module scope required). Explain the observed problem or desired outcome, include available reproduction evidence and verifiable acceptance criteria. Maintainer triage checks validity, duplicates, scope, relative priority and size; PR validation concerns the actual change and tests. See the [shared cubrid-lab writing standard](https://github.com/cubrid-lab/.github/blob/main/docs/ISSUE_PR_COMMIT_STANDARD.md).

**This does not change the CUBRID engine's JIRA issue process or its existing ticket-prefixed PR title, CLA and review rules.**

## How to file a bug report and suggest a new feature

  Please [our issue tracker](http://jira.cubrid.org/browse/CBRD) to [create an issue](http://jira.cubrid.org/secure/CreateIssue!default.jspa). 
  
  ### For a bug report
  
  * Please select a proper "Project". Typical choice is "CUBRID (CBRD)". 
  * Please specify "Issue Type" as "Correct Error" and describe your issues with details, especially a reproduction scenario.
  * It would be great if you also show us your expected results as well as the current results.
    
  ### For a feature suggestion
  
  * Please select a proper "Project". Typical choice is "CUBRID (CBRD)". 
  * Please "Issue Type" as "Improve Function/Performance" and let us hear your suggestion.
     
## How to submit a pull request

  We are using [the standard GitHub fork and pull requests workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962).

  If you want to submit your work to CUBRID, first please make sure that you have signed and submitted [the contributors license agreement (CLA)](https://github.com/CUBRID/cubrid/wiki/CUBRID-Contributor's-Agreement). 

  The workflow is essentially as follows:

  * Fork CUBRID project.
  * Make a topic branch. Make your changes to this branch.
  * Issue a pull request on CUBRID repository. Base branch for a pull request would be develop.

  You are kindly requested to keep your work mergeable. 

You can also refer to

  * [Forking a repository](https://help.github.com/articles/fork-a-repo).
  * [Using pull requests](https://help.github.com/articles/using-pull-requests/).
  * [How to Contribute to an Open Source Project on GitHub](https://egghead.io/series/how-to-contribute-to-an-open-source-project-on-github).
  
You can also send us an email to contact at cubrid.org.

## Code Review and CI Policy

The same pull request review criteria apply regardless of implementation
tool, including human-only work, OpenCode, Codex, Claude Code, ChatGPT,
Copilot and other agents. Optional AI reviews are advisory, not mandatory
tool-specific approvals. The existing CLA and `develop` base remain.

Use the repository's required GitHub Actions, Jenkins and CircleCI checks
(as configured for the change) as authoritative validation at the final PR
head. Local tests are recommended and should be reported accurately but
are not an extra merge condition. A maintainer reviews behavior, safety,
tests, compatibility and open findings, and makes the final merge decision.
Changes to CI credentials, authentication, security controls or publishing
require independent security and permission assessment. Do not weaken
existing branch protections or project-specific tests.


## Issue handoff and development progress

Use the issue and PR's actual state as evidence. Classification, authorization,
implementation, review and completion are **different decisions**:

1. **Intake / triage:** A newly filed issue starts with `status: needs triage`.
   Check evidence or reproduction, duplicate open/closed issues and overlapping
   PRs, repository scope, type, priority, size, dependencies, and verifiable
   acceptance criteria. A maintainer removes the intake label only after
   confirming the saved GitHub metadata. Do not infer priority, size, or triage
   completion automatically from the title or an AI suggestion.
2. **Ready:** Triage completion alone does not authorize development. Record
   the Ready decision in the issue only when the intended outcome and non-goals are bounded, blockers
   have been resolved, and any repository-specific product, architecture,
   safety or compatibility decisions have been accepted. Unresolved research
   remains investigation; blocked work records its dependency and next action.
3. **In Progress:** Before maintainer-directed or autonomous implementation,
   identify the actual implementer in the GitHub Assignee field, check whether
   another open PR already owns the change, and link the implementation PR to
   its issue. Human-led outside contributors may propose a change on an
   unclaimed issue without prior assignment or an AI-tool-specific approval;
   coordinate with existing assignees and follow the local contribution rules.
4. **In Review:** A PR is in review only when its scoped change and verification
   evidence are available. Check the required CI on the final PR head, test
   coverage appropriate to the risk, unresolved review findings and any
   repository-specific independent review or live-system validation. A bot
   review or passing CI cannot replace an outstanding product/safety decision.
5. **Done:** Record the actual disposition: a merged and validated change,
   a completed investigation with evidence, or an explained duplicate/not-
   planned closure. Use an issue-closing PR keyword only if merging actually
   satisfies its acceptance criteria. A merged PR is not proof that any
   deferred integration, fault, security or release verification has passed.

**Tracking without boards:** GitHub Issues and pull requests are the only
workflow tracker. The sole lifecycle label is `status: needs triage` for
unreviewed intake. Once triage is completed, remove that label after checking
the actual saved issue metadata; do not create `status: ready`, `status: in
progress`, or other duplicate workflow labels. Record the **Ready** decision,
remaining dependencies, and next action in the issue. For **In Progress**,
identify the actual implementer using Assignees and add a concise start/handoff
comment; link the working PR when it exists. **In Review** is visible from the
linked open, non-draft PR and its actual review/check status. A **Blocked**
issue records the blocker, responsible party, and unblock condition in a
comment. **Done** is the issue's Closed state with the recorded validated
outcome or explained disposition, not merely the existence of a merged PR.
Do not configure or depend on GitHub Projects/boards. Priority measures impact,
and size estimates effort; neither represents work-in-progress.
This guidance introduces no new automated merge gate and does not supersede
this repository's design, testing, security, or release requirements.

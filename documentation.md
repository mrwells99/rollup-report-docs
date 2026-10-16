---
title: Documentation
---


Roll-up Report shows how much work sits under each epic or parent issue: issue counts, % done, story points, original estimates, logged time and remaining time. You can also group by assignee, status or issue type, for any JQL.

## Where to find it
- **Project page:** open a project and choose **Roll-up Report** from the project's tabs (or the **More** menu). It shows the current project by default.
- **Dashboard gadget:** on a dashboard, choose **Add gadget**, then **Roll-up Report**. Set the JQL and grouping, then select **Save**.

## Using the report
1. Enter JQL, or leave it empty to use the current project. For example: `project = ABC AND sprint in openSprints()`.
2. Pick **Group by**: Epic / parent, Assignee, Status or Issue type.
3. Select **Run**. Columns can be sorted, and the last row is the total.

On a dashboard, the gadget shows a compact set of columns (issues, done %, points and logged hours) so it fits a narrow column.

## How totals work
- **Epic / parent:** each issue rolls up to its top-most ancestor in the results. Sub-tasks roll into stories and stories roll into epics. If an issue's epic isn't matched by your JQL, the issue still groups under that epic's key.
- An epic or parent whose children are in the results doesn't count toward **Issues** (its children are the work), but its own points and time are included. This applies in every grouping, so the issue total is the same however you group.
- **Done** means the issue's status is in the Done category.
- **Points** come from the site's "Story Points" or "Story point estimate" field.
- **Hours** come from Jira time tracking: original estimate, time spent (logged work) and remaining estimate.
- Reports cover up to 2,000 issues. If there are more, or the site is slow to answer, the report shows the issues it reached with a warning; narrow the JQL to get complete totals.

## Permissions
The app only reads Jira data (scopes `read:jira-work` and `read:jira-user`), and always as the person viewing the report. Nobody sees issues they couldn't already see in Jira.

## Support
Use the support contact on the app's Atlassian Marketplace listing. We aim to reply within 2 business days.

---
title: 'Campaigns  - Tips &amp; Hints'
subject: 'olh, SuiteCampaigns'
old_url: 'http://emarsys.dev/suite/online-help/ac-tips-hints/'
---

Here we have listed a number of suggestions as to how you can get the most out of the Automation Center. The tips have been grouped by functionality.

### Contents

- [Workflow tips](#workflow)
- [Program reporting](#reporting)
- [Opt-in for Transactional emails](#txm)<a name="workflow"></a>

#### Workflow tips

 Here is a collection of useful things which will help you whilst working on your blueprints.

- **Copying nodes** Press and hold CTRL and select one (or more) nodes on your workspace, and then move the mouse cursor to make a copy of the node(s). If you let go of CTRL whilst moving the mouse you will just move the nodes around the workspace.
- **Adding new nodes to active programs** If a program is active you can only add a new node to it by adding a new path; you cannot add one into an existing path.
- **Deselecting emails, forms or fields** If you have selected an item for a node, such as a form or an email, you can deselect it by opening the properties dialog, clicking **Select** and then **OK** without selecting anything. This will clear any previous selection. Note that the deselected item will only be available for selection elsewhere once you have saved the program.<a name="reporting"></a>

#### Program reporting

 Full program reporting, including goal definition and success criteria, is only available via the Smart Insight module. However, there are some easy ways to set up some simple reporting for yourself.

- **Using filters** If you add a **Wait** node and a **Filter** to the end of a path, you can measure the success of the path by whatever metrics you like. You can filter for straightforward responses, or measure specific database fields (such as total monthly revenue). For this reason many Blueprints already have filters at the end of their paths.
- **Using the Trends page** If you assign all the emails in a program to a category unique to that program, you can select that category in the [Trends analysis](/olh/analysis-trends.md "Analysis – Trends – General") and view the overall responses for the entire program. Since the emails are listed in chronological order according to their first launch, this will give a broad impression of contact participation through the workflow of the program.<a name="txm"></a>

#### Opt-in for translational emails

 When a transactional message is triggered by an Automation Center program, the first email will always abide by the opt-in status for the contact, except for programs using the following entry points:

- Form, e.g. Support request
- Abandoned shopping cart
- External event

 All other entry nodes will pay attention to the opt-in status, and can exclude contacts with status set to false. **Please Note**: The Automation Center program scheduling uses the account default timezone; please be aware that changing the timezone settings in the Suite Administrators page will not affect this.
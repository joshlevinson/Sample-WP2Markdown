---
title: 'Campaigns - Automation Center - Overview'
subject: 'olh, SuiteCampaigns'
old_url: 'http://emarsys.dev/suite/online-help/ac-overview/'
---

**Campaigns menu ->** Automation Center** On this page, you can view a list of existing programs, their status and creation date; you can also edit existing programs, view their summary after launch or delete them (if necessary).<a name="create"></a>

#### Create a program

 There are two ways to create a program:

1. **Create Blank Program** This opens the workspace for you to create your own program from scratch.
2. **Create Program From Blueprint** This displays the Blueprints dialog box, where you can:

- Use the Blueprint category menu to filter all the available preconfigured blueprints, e.g. based on Customer Lifecycle segment.
- Choose from a selection of blueprints; selecting one displays it in the Preview pane below

 Select the option you want and click **Create** to open the workspace. Here you have a menu on the left which contains all available [workspace nodes](/olh/workspace-nodes.md "Campaigns – Workspace Nodes"), plus a title and action bar at the top. Hover the mouse over the icons to get more information on what they do.

#### Name your program

 To name a brand new program, simply click the edit icon next to the title (default name is New Program #) and include a description.<a name="schedule"></a>

#### Schedule a program

1. Click the **Schedule** icon on the program Title bar and make your selection from the drop-down menu; you must specify a start date in the future.
2. Click **Set** **Schedule**.
 
**Attention**: Before a program can be scheduled, it must have passed all validation checks. Scheduled programs can be paused, in which case they will not become active when their start date is reached. If the start date has already passed when you re-activate the program, you receive a warning message that the program will start immediately, and you have the option to change the start date to a date in the future.<a name="settings"></a>

#### Make settings for contact participation

 Click the **Participation** icon on the program Title bar. Here you decide how frequently a contact can enter a program. There are three options:

- **At any time, but only once at a time** - Contacts can enter the program as soon as they have exited it, but not while they are still in it. There is no limit to the number of times a contact may enter under these conditions.
- **Only once ever** - Contacts can never enter this program twice.
- **At any time but only x days and x hours after exiting** - This builds in a delay so that contacts can only re-enter the program after a certain number of days or hours.

 The participation settings you define will also apply to the program when it is in testing. **Note**: One-time batch programs cannot have participation settings enabled due to their automated nature. **Attention**: ‘Contact’ here means unique contact ID. If an existing person is re-registered with the same email address but with a new ID they will not be excluded and could enter the program more than once.<a name="save"></a>

#### Save a program

 Click the **Save** icon on the workspace Actions bar. The Automation Center validates the program before saving. Any validation errors are displayed in the bottom right of the screen. The errors are displayed for a few seconds only, but you can pin them to the user interface by clicking the pin icon. Note: A program does not have to pass the validation check in order to be saved. It is a mere indication of the state of the program.<a name="validate"></a>

#### Validate a program

 For a program to be activated, it must fulfill a number of conditions. For example, all nodes must contain content, and must have the mandatory settings defined (e.g. subject line for emails). Every time you save a program, the validation errors are displayed in the bottom right of the workspace but not the program itself. Errors in program settings are checked and displayed on Activation.<a name="test"></a>

#### Test a program - Transactional Only

 Only programs which start with a transactional entry point (e.g. data change or form submit) can currently be tested. To test programs designed for individual contacts, enter the program in the expected way and provide an email address that is in the selected segment (i.e. is already in the database). If the email address is not in the test segment, the test will not work.<a name="test-paths"></a>

#### Test individual paths in a program

 You can test individual paths in a program by using the **Split Path** node. With this feature you can split any path and assign each of the test paths a % value. Contacts proceeding along the main path will be randomly distributed along the test paths according to these % values. You can add new paths and change the % value of existing paths at any time. However, you cannot delete a test path once contacts have passed along it. Once enough contacts have participated in your test and you are confident that you have an optimal choice, simply reduce the % values of the other paths to 0 and all future contacts will proceed along the remaining path. **Note**: There is no automated selection of success criteria for test paths. You should use filters or the [trends analysis](/olh/analysis-trends.md "Analysis – Trends – General") to determine which path is providing the best results for your program. To test different emails you must create a new email for each path. You cannot test different versions of the same email.<a name="edit"></a>

#### Edit programs

 Once a program has been activated, the degree to which it can be edited is reduced according to its state, but to edit just click the edit  icon.

#### Editing active programs

 When a program is active you <span style="text-decoration: underline;">can</span> do the following:

- Change the name and description
- Add nodes (only if new path is created)
- Change the end date in the scheduling
- Choose a different forms, segments and or email
- Edit the content of the form, or the filter conditions of the segment

 When a program is active you <span style="text-decoration: underline;">cannot</span> do the following:

- Remove nodes you have already saved
- Insert new nodes into a path
- Change the start date in the scheduling
- Change the participation settings
- Edit the content of an email (you can copy the email and edit the content, then select that email instead as a workaround. Editing an active email will be implemented in a future release).

#### Editing scheduled programs

 When a program is active but scheduled you can edit it as described above for active programs, and also do the following:

- Change the start date in the scheduling
- Change the participation settings
- Edit the content of the email

#### Editing paused programs

 When a program has been paused you can edit it according to its state when it was paused, i.e. active or scheduled.

#### Editing finished programs

 Once a program has finished you will not be able to edit any part of it.<a name="activate"></a>

#### Activate a program

 Clicking **Launch** in the **Program Status** drop-down starts the program, unless a start date in the future has been entered. Provided all validation checks have been passed, the program is now live and contacts can enter and progress along it as expected. Once a program is active, there are a number of [other actions](/olh/about-the-ac.md "Campaigns – About the Automation Center") you can perform in the **Program Status** drop-down.<a name="delete"></a>

#### Delete a program

 To remove a program, go to the Program List and click the X icon next to the item you want to delete. Programs can only be deleted if they have not yet been activated, and are not currently under Testing (i.e. they have to be in the in Design state.) Deleting the program will free all associated resources (forms, fields, emails, etc.) for use in other programs. The exception to this are emails which have already been launched during a test. To re-use these emails you must copy them. Important Notes on Editing

- Any validation errors caused by changes will cause the save to fail - but not undo the changes which allows you to address them.
- Before saving you have the option to discard all changes, but this cannot be undone if you accidentally save unwanted changes.
- If your program has responses, then selecting another email will render the response invalid and a new one must be manually selected.

 To see a summary of a program click on the view [![view_details_icon](/assets/images/view_details_icon.png)](/assets/images/view_details_icon.png) icon to get to the [Program Summary](/olh/program-reporting.md "Campaigns – Program Reporting") section.

**
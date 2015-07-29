---
title: 'Campaigns - About the Automation Center'
subject: 'olh, SuiteContacts'
old_url: 'http://emarsys.dev/suite/online-help/about-the-ac/'
---

**Campaigns** menu -> **Automation Center**#### What is a program?

 A program is a series of actions, starting from an entry point and progressing along a decision tree until an end point. A program may have multiple entry points, multiple paths and multiple end points. Once a contact has entered a program, they can progress along one path only until the end. Their trajectory along the program is determined either by their actions or by filters applied by you. Programs can be activated manually or scheduled to become active at a specified date in the future. Similarly, they can be deactivated manually or scheduled to stop at a certain time. Contacts can enter and progress along a program only when the program is active. #### What types of programs can be created?

 Programs can be differentiated in two ways: by their type and by their objective. The type refers to the program structure, the objective refers to whether the program goal relates to customer life cycle management, or if it is simply operational. Once a program finishes any elements used in the program are available to be reused in other programs (e.g. entry point, data field, etc.). You can create the following program types: - **Transactional programs**

These are emails that are triggered by a specified action and sent to a single contact, typically with a single, limited objective, e.g. a purchase confirmation. Transactional programs start with the following entry points: Form submit, Data change, New contact, External event, Abandoned shopping cart and build from there.

- **Recurring programs**

These are emails which are regularly launched according to a predefined schedule and to the same recipient list or segment, e.g. a monthly newsletter or daily deals.

Recurring programs start with the Recurring filter and Recurring email entry points.

- **Ad hoc batch programs**

These are email campaigns launched at a specified time to a specific list or segment, and which can contain follow-up steps according to a defined schedule or based on contact responses, e.g. seasonal offers, event invitations, product launches. Ad hoc batch programs start with the Target filter and Batch email entry points.

 Program can also have different objectives: - **General purpose programs**

These are concerned with administrative (e.g. shipping confirmation) and revenue generating (e.g. deal of the day e-mails) tasks.

- **Customer lifecycle programs**

These relate to targeting based on customer behavior and aim to maximize customer retention. The different customer lifecycle stages are reflected in the blueprint categories.

#### What is a blueprint?

 Blueprints are the visualization of the idea for a program which is made up of a series of workspace nodes which you can modify, expand and build on to create a certain information flow when certain conditions are met. Blueprints are categorized according to their objective, rather than their nature or content. This means that many of them will look identical, but their descriptions will suggest different content to help reach a different goal. #### Preconfigured blueprints

 In the Blueprints dialogue box you have the option to filter the preconfigured blueprints by their purpose using the Blueprint category drop-down menu. The blueprints are classified as either being related to customer lifecycle stages, or as general purpose blueprints. In the customer lifecycle group, you can further filter according to the relevant stage: Leads, 1st time buyers, Active buyers, Defecting customers or Inactive customers. #### What are workspace nodes?

 Workspace nodes are placeholders for  functions with customizable variables that you can define, and are split into three types, available via the Automation Center toolbar: - **Entry Points** are how the contacts enter the program. They can be triggers (e.g. form submit, API call), scheduled events (e.g. recurring filters), or ad hoc actions (e.g. bath email). A program can have multiple entry points if the logic flow permits.
- **Responses** are specific checks which are directly linked to the previous node in the path. For example, if the response ‘didn’t click link’ is put after an email, the links from that email will automatically be displayed in the node properties. The user can therefore select them without having to search for the email first.
- **Actions** are actions taken by the Automation Center to guide the contact through the program.
 
 All nodes have a **Properties** page where you can select the content (i.e. form, segment, email, etc.), preview and edit content by double clicking on the node. Workspace nodes can be deleted and connected by clicking the corresponding buttons on the Workspace Actions bar. **Note**: An email will only be available for selection if 'in Design' state and not currently in use by another program. Once the program is saved the email is assigned which changes the text under the email icon from description (unsaved) to email name (saved). Once the program is active you cannot edit the content of an email, nor delete a segment, form or email that is used by the active program. #### Which actions on programs can I perform?

 You can perform the following actions on a program: - **Test** - This puts the program to the state 'In testing'. A program can only be tested if it has passed all validation checks. Transactional Programs Only!
- **Launch** - This puts the program to the state 'Active'. A program can only be activated if it has passed all validation checks.
- **Pause** - This puts the program to the state 'Paused'. Only 'Active' or 'Scheduled' programs can be paused. If a program is paused, all contacts in it are queued and processed when it is reactivated. Contacts that would normally enter the program during this time are also queued and enter it when it is active again.
- **End** - This closes the program to new contacts but allows those already in it to progress and complete their journey.
- **Abort** - This stops all activity in the program, closes it to new entrants and discards all contacts already in the program.

#### Which states can a program have?

 The state of a program is displayed on the right of the Workspace Actions bar. To change it, select another option from the drop-down menu. The following states are available: - **In design** - The program is currently being worked on and has not yet been activated. The program is fully editable.
- **In testing** - Test mode has been turned on. The program must pass all validation checks before it can enter test mode. Participation settings are taken into account during testing, scheduling is ignored.
- **Active** - The program is complete and has passed all validation checks. Contacts can enter the program, progress along it as defined, and actions and responses are tracked for reporting.
- **Paused** - The program has been paused; you can make some limited changes to the content or check the initial results. Both Active and Scheduled programs can be paused.
- **Finished** - Once a program reaches the end point defined in the **Scheduling** dialog box, it is finished. No more contacts can enter the program, but the contacts in the program can continue to progress along it until they exit it one way or another (unless the program has been ended manually via the End Program control). Finished programs cannot be edited or reactivated.
- **Scheduled** - The program has been activated via **Activate** function, but has a start date that is in the future. All settings for scheduled programs can be fully edited.
- **Aborted** - The program has been aborted and all contacts in it discarded. Aborted programs cannot be edited or reactivated.
 
 Once you are done with the design and start testing your program, the Automation Center canvas outline changes color to give you an indication of what the state is, including: - **Purple** - In testing
- **Yellow** - Paused
- **Green** - Scheduled, Active and successfully Finished
- **Red** - Error state
- **Black** - Aborted
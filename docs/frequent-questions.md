# Frequently Asked Questions

## General


??? question "How do I install the plugins?"
    Email us at [ info@termite.tools ](mailto:info@termite.tools). We will provide you a link with the installation guide for each specific CAD software.
---
## Sessions

??? question "What is a session?"
    A session works as a directory where you can save your list of spaces and areas, sync Termite with a CAD software, and generate variations of layouts. It acts as a new chat for ChatGPT.

??? question "How can I add a session?"
    Open the Termite dashboard and click on **start a new session**. You can define a name for your sessions and click on **create**. Follow instructions on [starting a session](sessions.md/#generate-your-first-session).

??? question "How many sessions do I need to have?"
    It depends on your preference. You can work on different projects in one session or different sessions. It depends on how you prefer to have a single directory or group your work into directories. This is similar if you prefer to have all your questions to ChatGPT is one chat or in different chats. Both ways you will have access to all your data.

??? question "How can I switch between the sessions?"
    On the left side of the Termite dashboard, you can find a **Navigation** tab. Under the **History** you can see a list of your created sessions and can click on each session to work on.

??? question "How can I enter the spaces?"
    On the Termite dashboard, navigate to **physical program** tab and there you can see different options for adding a new space. You can select from a template or add new space names and areas. Either way you can edit the spaces afterward. Follow instructions on [how to add new spaces](sessions.md/#physical-programs).

??? question "Can I save the space lists and areas in a session?"
    Yes, you can download your list of spaces as a **CSV file**. This can be used later for other projects. Follow instructions on [saving your spaces](sessions.md/#reusable-templates).

??? question "Can I reuse the saved space lists and areas in another session?"
    Yes, you can reuse your saved **CSV file** including your space names, areas, and other assigned characteristics. Follow instructions on [reusing your saved spaces](sessions.md/#reusable-templates).

??? question "Can I rename a session?"
    This feature will be added soon.

??? question "Can I delete a session?"
    This feature will be added soon.


---
## Integrate with CAD software
??? question "With which CAD software Termite can be integrated?"
    Termite can be integrated with [Rhino](Integrate Sessions with CAD Software/rhino/index.md), [Grasshopper](Integrate Sessions with CAD Software/grasshopper/index.md), [Revit](Integrate Sessions with CAD Software/revit/index.md), and [Archicad](Integrate Sessions with CAD Software/archicad/index.md).

??? question "How can I sync a session with my CAD software?"
    Follow the instructions for syncing your session with each of the CAD software: [Rhino](Integrate Sessions with CAD Software/rhino/sync-index.md), [Grasshopper](Integrate Sessions with CAD Software/grasshopper/sync-index.md), [Revit](Integrate Sessions with CAD Software/revit/sync-index.md), and [Archicad](Integrate Sessions with CAD Software/archicad/sync-index.md).

??? question "How should I set design inputs and sync them with Termite?"
    Termite gets design inputs including **boundary**, **space location points**, and **fixed spaces** from CAD software. Follow instructions on how to [set inputs for Rhino](Integrate Sessions with CAD Software/rhino/sync-index.md/#sync-a-termite-session-with-rhino), [set inputs for Grasshopper](Integrate Sessions with CAD Software/grasshopper/sync-index.md/#sync-a-termite-session-with-grasshopper), [set inputs for Revit](Integrate Sessions with CAD Software/revit/sync-index.md/#sync-a-termite-session-with-revit), and [set inputs for Archicad](Integrate Sessions with CAD Software/archicad/sync-index.md/#sync-a-termite-session-with-archicad)

??? question "Why I cannot sync my boundary curve with a Termite session?"
    The boundary curve needs to be a **closed curve**, otherwise it cannot be synced with Termite.

??? question "Can I change the design inputs and regenerate a layout?"
    Yes, this is the power of Termite. Simply update your design inputs and select them again and submit the changes to be synced with a Termite session. Follow instructions on [how to generate design variations in Rhino](Integrate Sessions with CAD Software/rhino/generate-index.md/#exploring-design-variations), [how to generate design variations in Grasshopper](Integrate Sessions with CAD Software/grasshopper/generate-index.md/#exploring-design-variations), [how to generate design variations in Revit](Integrate Sessions with CAD Software/revit/generate-index.md/#exploring-design-variations), and [how to generate design variations in Archicad](Integrate Sessions with CAD Software/archicad/generate-index.md)

??? question "Can I add walls, doors, windows, and balcony railings to a layout?"
    Yes, through the Termite dashboard. Select a generated layout and on the left tab navigate to **Drafting**. You can add walls, doors, windows, and balcony railings there. Follow instructions for [Rhino](Integrate Sessions with CAD Software/rhino/generate-index.md/#next-steps-in-generating-a-layout), [Grasshopper](Integrate Sessions with CAD Software/grasshopper/generate-index.md/#next-steps-in-generating-a-layout), [Revit](Integrate Sessions with CAD Software/revit/generate-index.md/#next-steps-in-generating-a-layout), and [Archicad](Integrate Sessions with CAD Software/archicad/generate-index.md)

??? question "Can I change the size of the wall trim, doors, and windows?"
    Yes, in the drafting tan under each of the sections for **walls**, **doors**, **windows** you can change the size. 

??? question "Why I cannot add more wall trims, doors, and windows?"
    This happens when you have already confirmed your drawing. Simply press **shift** and you will be able to add more drawing as **wall trims**, **doors**, **windows**, and **balcony railings**.

??? question "How can I delete some wall trims, doors, windows, and balcony railings?"
    Simply select the **wall trims**, **doors**, **windows**, and **balcony railings** that you want to delete and press **delete button** on the keyboard.

---
## Export

??? question "How do I export to DWG?"
    See the [DWG export guide](export/dwg-index.md).

??? question "How do I export to BIM?"
    See the [BIM export guide](export/bim-index.md).

??? question "Can I design with Rhino and sync with Termite and later export as BIM model?"
    Yes, exporting is not dependent on the original CAD software. By using each of the CAD software you can export as either DWG file or BIM model. [Follow instructions here](export/index.md)





# Inventory-Check-Automation using n8n.
Workflow that checks stock every week and alerts the team before items run out.
=> It prevents stockouts, reduces manual work, saves money instantly.

# How is it done ? :
First adding The Trigger.
Data is retrieved from Google Sheets (Step 2) and verified as JSON (Step 3).
Logic is implemented: We added and validated the Filter Node that cut out all the noise (Steps 4 and 5).
Output is merged in one item (Step 6).

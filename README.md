# Inventory-Check-Automation using n8n.
Workflow that checks stock every week and alerts the team before items run out.
=> It prevents stockouts, reduces manual work, saves money instantly.

# How is it done ? 
First adding The Trigger.
Data is retrieved from Google Sheets (Step 2) and verified as JSON (Step 3).
Logic is implemented: We added and validated the Filter Node that cut out all the noise (Steps 4 and 5).
Output is merged in one item (Step 6).

# Making the flow intelligent :
Integrate the AI agent with the prompt :

Act as a diligent, professional Inventory Control Assistant for a restaurant supplier.
Your task is to generate and send one concise alert message to Gmail listing all items where stock is below the threshold.

Data:
{{JSON.stringify($json)}}

Output format:
Start with: "⚠️ Low Stock Alert:"
Then list each item on a new line in this format:
- [Item Name]: [Stock] left (need [Threshold]). Recommend reordering from [Supplier] to maintain adequate stock levels.

Rules:
- If stock is 0, say "Out of stock" instead of "[Stock] left".
- Do not add summaries, explanations, or closing sentences.

# Workflow : 

![insventoryCheckMailingAlert](https://github.com/user-attachments/assets/c05f04aa-1974-4509-adf8-c1461990c2a6)





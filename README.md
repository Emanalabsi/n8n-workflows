# n8n Workflows 


### Warehouse Filter
> Pulls order data from a company data warehouse, filters the records that matter, and automatically notifies the right people with the results.

 I used an HTTP Request node to pull order data from a company data warehouse, then used IF and Switch nodes to filter the records based on conditions. 


---

### Daily News Digest
> Every weekday at 9AM, this workflow fetches the top 5 live news headlines and delivers a clean formatted email to my inbox automatically.

 I used a Schedule Trigger set to weekdays at 9AM, an HTTP Request node with query parameters to fetch live headlines from NewsAPI, a Code node to format the data into clean HTML, and Gmail to deliver it automatically every morning. 


---

### Team Pulse
> Every Friday at 5PM, this workflow automatically reads my weekly work logs, uses AI to write a professional status report, and emails it to the manager.

 I used a Schedule Trigger to run every Friday at 5PM, Google Sheets to read my weekly logs, a Code node to process the data with JavaScript, an HTTP Request to call the Groq AI API using JSON.stringify() to handle the request correctly, and Gmail to send a formatted HTML email automatically. I also added an IF node for empty sheet protection and a separate Error Workflow for failure alerts.


---
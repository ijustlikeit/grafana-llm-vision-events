## **Grafana LLM vision event panel**.

Grafana based panel that shows full list of LLM vision events.  This is another way to view the events captured by LLM vision integration for Home Assistant.  Check out this excellent integration @
https://llm-vision.gitbook.io/getting-started .  

Here is a sample of the Grafana LLM event table panel as a dashboard in Home Assistant:

<img width="1426" alt="Screenshot 2025-03-28 173338" src="https://github.com/user-attachments/assets/cca34928-75a0-4bca-be86-07897c4f3478" />

You can filter on any column which gives you maximum flexibility in viewing historical events of your choosing.

## **Prerequisites**

1. Home Assistant
2. LLM Vision integration
3. Grafana Add-On

## **Installation**

1. Start Grafana. Install plugin *fser-sqlite-datasource*.  This can be done by editing the Grafana add-on Configuration tab and adding fser-sqlite-datasource in the plugin section and restarting.
2. From the Grafana menu select  **Add new connection**. Find the Sqlite source box  from the list and click on it.
3. From the Grafana menu select  **Data sources**. Add a new data source. Under settings input: _Path: /config/llmvision/events.db_. Save and test.
4. Select **Data sources** again. Hover mouse over the fser-sqlite-datasource entry.  Look for the URL at the bottom of the screen. Take note of the text at the end of the URL after the edit/ part. This is the uid for this datasource. Save it.
5. Download the **llm-vision-events.json** file from this repository.
6. Edit **llm-vision-events.json**.
   - Line 136. Replace the URL with your home assistant URL.
   - Line 691. Replace the uid with step 4 uid.
   - Save the file.
7. Select **Data sources** again. Select Build a dashboard from the fser-sqlite-datasource.  Select **Import dashboard**. If you see "Unsaved dashboard.." discard.
8. Upload **llm-vision-events.json** file.
9. At this time you should see the Events panel.
10. You can edit this Grafana panel and change things as you prefer (click three ... top right hand corner).
11. Create a share link that you can use to insert into a home assistant dashboard Webpage card. (click three ... top right hand corner and Share; Share link: copy link)

## **Extras**

1. Enable **Kiosk mode** top corner 2nd icon from right for a nice clean look.


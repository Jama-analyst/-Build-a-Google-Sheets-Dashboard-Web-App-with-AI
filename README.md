# Build a Google Sheets Dashboard Web App with AI (No Code)
In this guide, I will show you how to use AI to build a custom, interactive Web App Dashboard directly from your Google Sheet data. By simply copying a prompt into ChatGPT or Gemini, you can generate the code for a dashboard that runs entirely for free, looks like premium software, and serves as a perfect lightweight alternative to Looker Studio.

## Table of Contents
Why build a Google Sheets Dashboard Web App this way?
- Prerequisites: What You Need Before Starting
- The AI Prompt & How to Use It
  - Step 01: How to Feed Your Data to the AI
  - Step 02: The AI Prompt
- The Generated Code (Reference)
- How to Implement the Code
  - Where to place the code
  - Create your files
  - Deploy the Web App
  - View Your Dashboard
  - Pro Tip: Build Gradually, Don’t Overload
- Next Steps: Customizing Your Dashboard (No Code Needed)
- Wrapping Up

## Why build a Google Sheets Dashboard Web App this way?
- Before we dive into the “How,” let’s look at the “Why.” Why not just use Looker Studio or standard Sheet charts?
  - 100% Free & Native: It runs entirely on Google’s servers. No external subscriptions.
  - Interactive Web App: This isn’t just a picture of a chart. It’s a deployed website URL that you can share with your team.
  - Total Customization: Since we are generating the code, you can tweak colors, layouts, and logic to fit your exact needs.
  - Data Security: Your data stays within your Google account.

## Prerequisites: 
- [ ] What You Need Before Starting
You don’t need to be a coder, but you do need your data ready.
1. A Google Sheet with Data: Ensure your data is in a clean format.
- Row 1: Headers (e.g., “Date”, “Sales”, “Region”).
- Rows 2+: Your actual data.
- No Merged Cells: Ensure the data looks like a standard table. 
2. An AI Chatbot: Gemini, ChatGPT, or Claude.

## The AI Prompt & How to Use It
The secret to success isn’t just asking AI to “make a dashboard.” It is about providing technical constraints so the AI writes clean, error-free code.
I have refined a prompt that forces the AI to use best practices (like server-side normalization and separate HTML files).
- [ ] Step 01: How to Feed Your Data to the AI
- To get working code, the AI needs to know your column structure (e.g., “Column A is Dates, Column B is Sales”). You have three ways to do this:
  - Option A: Use the “Add Files” option of your chatbot, and chose the Google Drive option, and select the Google Sheets Workbook (Make sure your data is in the first tab of the Google Sheets Workbook)
  - Option B: Download your sheet as a CSV file (File > Download > Comma Separated Values) and upload it directly to the chat window.
  - Option C: Highlight your headers and the first ~10 rows of data. Copy them and paste them directly into the prompt below.

- [ ] Step 02: The AI Prompt
- I have designed a specific prompt that forces the AI to use best practices—like separating HTML from logic and normalizing data so your charts don’t break.
- In this prompt, I am asking the AI to decide the type of charts to be included in the dashboard. You can modify the code and request the type of charts you need.
- Copy and paste this prompt into ChatGPT, Claude, or Gemini:

[The AI Prompt](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/The%20AI%20Prompt.pdf)

## The Generated Code (Reference)
The AI will generate custom code tailored to your data. However, the structure will be similar to the example below. If you want to test this right away, you can use the generic template provided. You can copy the Google Sheet containing the data from the link below to your Drive.

## The generated codes comprise the following four files (as requested in the prompt).
- The Server Logic (Code.gs): This script fetches data from your sheet and serves the webpage.

[Code.gs](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Code.gs.pdf)  

- The Layout (Index.html): This is the skeleton of your dashboard, using Bootstrap for a responsive, mobile-friendly grid.

[Index.html](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Index.html.pdf)

- The Logic (JavaScript.html): This handles drawing the charts.

[JavaScript.html](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/JavaScript.html.pdf)

- The Styling (css.html).
  
[css.html](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/css.html.pdf)


## How to Implement the Code
Now that the AI has generated the necessary components, we can proceed with building the dashboard.
- [ ] Where to place the code
- If you haven’t used Google Apps Script before, you might be wondering where to paste the code above.
  
Google Sheets contains a powerful tool called Google Apps Script (similar to VBA in Excel). You can access the editor directly from your spreadsheet menu.
1. Open your Google Sheet.
2. Navigate to Extensions > Apps Script.

- [ ]  Create your files via Apps Script
- Once the AppsScript editor opens, you will see a default file named Code.gs. However, our AI prompt requested a structure with four separate files to keep things organized.
- We need to manually create the HTML files in the editor:
1. Clean Code.gs: Delete the default code inside the existing Code.gs file and paste the server-side code provided by the AI.
2. Create HTML Files:
   - On the left sidebar, click the + (Plus) icon next to “Files”.
   - Select HTML from the dropdown.
[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%201.png)
[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%202.png)
[[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%203.png)

   - Name the file Index (Apps Script automatically adds .html, so just type “Index”).
   
   - Repeat this process to create two more HTML files named JavaScript and css.
[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%201.png)
[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%202.png)
[[Creating Files](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/Creating%20Files%20under%20Apps%20Script%203.png)

3. Paste the Code: Open each file you just created and paste the corresponding code generated by the AI.
4. Save: Click the Disk icon in the toolbar (or press Ctrl + S / Cmd + S) to save your project.
![image](https://github.com/Jama-analyst/Sales-Performance-Web-Dashboard/blob/main/Sales%20Performance%20Dashboard.jpeg)
   
- [ ]  After creating all 4 files, your file structure should look like the one below.
![image](https://github.com/Jama-analyst/-Build-a-Google-Sheets-Dashboard-Web-App-with-AI/blob/main/HTML%20Files%20Structure.png)




## Deploy the Web App
This is the step where your script transforms into a live dashboard URL.
- Click the blue Deploy button in the top-right corner.
- Select New deployment.
- Click the Gear icon next to “Select type” and choose Web app.
- Fill in the configuration settings:
  - Description: Enter a name (e.g., “Sales Dashboard v1”).
  - Execute as: Select Me (your email address).
  - Who has access: Select Anyone with Google Account (if you want to share it internally) or Anyone (if you want it fully public).
- Click Deploy.
![image](https://github.com/Jama-analyst/Sales-Performance-Web-Dashboard/blob/main/Sales%20Performance%20Dashboard.jpeg)

https://script.google.com/macros/s/AKfycbyRFSuC9dqi8JdRkRRscSzao6hzmFKF5R2ZCkCWvY6dKzuBqBl3-VkYEN-ftPpbwXTpAg/exec




## Since this is the first time running the script, Google will ask for permission to read your spreadsheet data.
- Click Authorize access.
- Select your Google account.
- Important: You may see a screen saying “Google hasn’t verified this app.” This is normal because you are the developer.
- Click Advanced.
- Click Go to (Untitled Project) (unsafe) at the bottom.
- Click Allow.
  
## View Your Dashboard
Once authorized, Google will provide you with a Web App URL.

Click that link to open your new dashboard in a full browser tab. You can bookmark this link and share it with anyone. Whenever you update the data in your original Google Sheet, simply refresh this webpage to see the charts update instantly.

You can view the live dashboard from this link.

![image](https://github.com/Jama-analyst/Sales-Performance-Web-Dashboard/blob/main/Sales%20Performance%20Dashboard.jpeg)

## Next Steps: Customizing Your Dashboard (No Code Needed)
Once your base dashboard is live, you can simply ask the AI to upgrade it. Keep the chat open and try these iterations:
- Add Interactivity (Dropdowns): The real power of a web app is interactivity. Ask the AI to make the charts dynamic.
- Prompt: “Update the code to add a dropdown menu at the top. When I select a specific ‘Region’, update all charts to show data only for that region.”
- Visual Polish: Once the logic works, fix the look.
- Prompt: “Update the CSS to use a ‘Dark Mode’ theme and change the charts to my brand colors: Navy Blue and Gold.”
By layering these features step-by-step, you ensure your dashboard remains stable and error-free while becoming increasingly powerful.

![image](https://github.com/Jama-analyst/Sales-Performance-Web-Dashboard/blob/main/Sales%20Performance%20Dashboard.jpeg)

## Wrapping Up
Building a custom dashboard used to require a budget for developers or a subscription to expensive BI tools. Today, all it took was your data, a smart prompt, and a few minutes of copy-pasting.
You now possess a powerful new skill: the ability to turn raw numbers into a shareable, interactive experience. Whether you use this for client reporting, internal team tracking, or just to organize your personal finances, the flexibility is unmatched because you own the code.
Don’t stop here. The web app you just deployed is a living foundation. As your data grows and your needs change, simply return to your AI assistant to add new filters, tweak the design, or expand the logic. The technical barrier is gone—now it’s time to create.  

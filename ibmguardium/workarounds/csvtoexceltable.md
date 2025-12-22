<h1>IBM Guardium CSV Data Import Guide</h1>
Instead of directly tabulating the CSV file downloaded by IBM Guardium, you can obtain a cleaner table by importing it as data and adjusting the data types.

1. Downloading the CSV File Download the relevant CSV file from the IBM Guardium interface. The downloaded file will be named filename.csv and will be saved to your computer's Downloads folder.
<img width="945" height="449" alt="image" src="https://github.com/user-attachments/assets/41f4378d-0824-4a82-a801-fd63d6eb37e2" />

2. Opening a New Sheet in Excel Open Microsoft Excel and create a new blank worksheet. This sheet will be used to import your CSV data.
<img width="559" height="277" alt="image" src="https://github.com/user-attachments/assets/185358fc-d0aa-410d-aecc-2e4d4816c7e2" />

3. Starting the Data Import Process Click on the Data tab from the Excel menu bar. Then, select the From Text/CSV option to start the import process. 
   - Note: In the file selection window, find and select the filename.csv file you downloaded earlier.
<img width="945" height="371" alt="image" src="https://github.com/user-attachments/assets/f99929c4-8d01-49d8-a991-d060181db669" />

4. Selecting the "Transform Data" Option Click the "Transform Data" button on the preview screen that appears after the CSV file loads. This option will open the Power Query Editor and allow you to edit data types.
<img width="945" height="704" alt="image" src="https://github.com/user-attachments/assets/e27f156c-5200-4cc0-a3d8-08fadbbc67e9" />

5. Opening the Advanced Editor After the Power Query Editor opens, click the arrow icon in the top right corner (marked with number 1) to expand the advanced settings tab. This will allow you to edit the M code.
<img width="850" height="414" alt="image" src="https://github.com/user-attachments/assets/8ce46624-257d-4139-89ee-b8fb2d03f3de" />

6. Editing Data Types Find the Int64.Type expressions within the code in the Advanced Editor and change them to type text. This ensures that data, especially IP addresses, is displayed correctly.    
  - Code Change:
    
<code>Before: {"Client IP", Int64.Type}</code>

<code>After: {"Client IP", type text}</code>


⚠️ <b>Attention: Ensure that you change all Int64.Type expressions to type text. This process must be done manually.</b>

7. Completing the Process After completing all edits, click the "Close and Load" button in the top left corner. This action will transfer your data to the Excel table and display it in the edited format.

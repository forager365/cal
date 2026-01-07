# On-Call Schedule Calendar

A web-based calendar application to view and manage on-call schedules with Outlook integration.

## Features

- One month per page calendar view with navigation
- Shows on-call schedules for 6 people with unique color coding
- Navigate between months using Previous/Next buttons
- Dropdown filter to view schedules by person
- Export to Outlook calendar (.ics format) for all months
- Responsive design for mobile and desktop
- Today's date highlighted in yellow
- Weekend dates (Saturday & Sunday) highlighted with pastel blue background
- Color-coded legend for easy identification
- Soft pastel color scheme for comfortable viewing
- Self-contained single HTML file - perfect for GitHub Pages deployment

## Files

- `index.html` - Main calendar web page (contains embedded schedule data)
- `oncall-schedule.csv` - Reference CSV file (for manual editing before embedding)

## How to Use

1. **Open the Calendar**
   - Simply open `index.html` in any modern web browser
   - The calendar will automatically load from embedded data
   - Current month is displayed by default

2. **Navigate Between Months**
   - Use the "Previous Month" and "Next Month" buttons to view different months
   - The current month and year are displayed in the center

3. **Filter by Person**
   - Use the dropdown menu at the top to select a specific person
   - Select "All People" to see everyone's schedules

4. **Sync to Outlook**
   - Click the "Sync to Outlook Calendar (All Months)" button
   - An `.ics` file will be downloaded containing all schedule data
   - The sync respects the person filter (if you filtered by Alice, only Alice's events will be synced)
   - Open the file to import events into Outlook or any calendar app

## Deploy to GitHub Pages

1. Upload `index.html` to your GitHub repository
2. Go to repository Settings → Pages
3. Select the branch and folder where `index.html` is located
4. Save and wait for deployment
5. Access your calendar at `https://yourusername.github.io/repository-name/`

## Updating Schedule Data

The schedule data is embedded directly in the `index.html` file. To update it:

1. Edit the `oncall-schedule.csv` file with your schedule data:
   ```
   name,email,date
   Alice Johnson,alice.johnson@example.com,2026-01-06
   Bob Smith,bob.smith@example.com,2026-01-07
   ```

2. Open `index.html` in a text editor
3. Find the `const csvData = \`...\`` section (around line 298)
4. Replace the embedded data with your CSV content
5. Save and upload to GitHub Pages

### CSV Format

- **name**: Person's full name
- **email**: Person's email address
- **date**: Date in YYYY-MM-DD format

## Browser Compatibility

Works with all modern browsers:
- Chrome/Edge
- Firefox
- Safari
- Opera

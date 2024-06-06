# Internship Tasks

## Task 1: Email Sender System

### Step 1
- Configure Exchange Email.
- Configure Database.
- Fetch only unseen emails from the mailbox.
- Parse emails to extract:
  - Sender's name
  - Email address
  - Subject
  - Body
  - Received time
- Extract phone numbers from the email body (if present).
- Clean the email body to remove extra text.
- Save the parsed data into a database.
- Handle attachments:
  - Allow attachments with size < 2 MB and file types jpeg, jpg, png, pdf.
  - Save issues related to attachments in the `attachment_issue` column.
- Mark processed emails as seen.

### Step 2
- Fetch data from the database.
- Process only unprocessed and current date emails stored in the database.
- Convert email attachments into base64 format.
- Convert processed data into JSON format.
- Call an API to pass the processed data.
- Update the `processed` column for emails that have been processed.
- Add the issue ID returned by the API to the `issue_id` column.
- Delete all attachments that are 15 days older than today's date.

### Step 3
- Create a cron job to schedule this task.
- Adjust schedule time to 5 minutes.

## Task 2: Enable Email Cron Job for Mantis BT
- Enable Email cron job from `configure_default_inc`.
- Create a cron job and schedule it.

## Task 3: Migrate Attachments from Database to Disk Storage
- Change attachment storage from database to disk in `configure_default_inc`.
- Update the path for storing attachments on disk.
- For old attachments:
  - Go to Admin Portal.
  - Select System Utilities.
  - Click on 'Move Attachments' Button.

## Task 4: Integrating and Troubleshooting Plugins

### Task 4(a): Holiday Plugin
- Fix bugs.
- Modify files to ensure compatibility with Mantis BT.
- Integrate with Mantis BT.
- Ensure the plugin reassigns issues to backups when an officer is on holiday.

### Task 4(b): Trigger Close Plugin
- Merge 2 to 3 outdated plugins into a functional plugin.
- Integrate with Mantis BT.
- Automatically close issues that are resolved or have no feedback after 15 days.

### Task 4(c): Add Due Date Plugin
- Fix bugs.
- Troubleshoot and resolve issues in this plugin.
- Integrate with Mantis BT.
- Assign due dates to issues based on priority level.

### Task 4(d): Reminder Plugin
- Integrate with Mantis BT.
- Send reminder emails when the due date is approaching.

### Task 4(e): Query Plugin
- Fix bugs.
- Troubleshoot and resolve issues in this plugin.
- Integrate with Mantis BT.
- Write a query to generate a report.
- Create an HTML/CSS template for the report.

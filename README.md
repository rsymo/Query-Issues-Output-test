# Query-Issues-Output-test
https://github.com/marketplace/actions/query-issues-output

# Using a combination of GitHub Actions in a Workflow file to:
- Search for Issues that match a Filter, in a specific repo
- Download a JSON file for each issue that matches the query
- Zips up all the issue JSON files
- Sends an email (via Gmai) that contains the zip file as an attachment 

# The workflow file is here:
https://github.com/rsymo-org/Query-Issues-Output-test/blob/main/.github/workflows/main.yml

# To make this work:
1. Setup Repository secrets for: 
- RECIPIENT_EMAIL_ADDRESS - your email; or whereever you want the zipped issue JSON files to be emailed to
- MAIL_USERNAME - Gmail account username
- MAIL_PASSWORD - Gmail token - some info: https://devanswers.co/create-application-specific-password-gmail/
- TOKEN - your GitHub PAT - docs: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

2. Create some sample issues, and run a test query to ensure it works ok.
- This workflow uses this action, so best to understand query capabilities directly from the source: https://github.com/marketplace/actions/query-issues-output



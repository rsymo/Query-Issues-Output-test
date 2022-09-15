# GitHub workflow built from a combination of GitHub Actions available on the marketplace to:
- Search for Issues that match a Filter in a specific Repo
- Download a JSON file for each issue that matches the query
- Zip up all the JSON files
- Send an email (via Gmail) that contains the zip file as an attachment 

# The workflow file is here:
https://github.com/rsymo-org/Query-Issues-Output-test/blob/main/.github/workflows/main.yml

# To make this work:
1. Setup Repository secrets for: 
- RECIPIENT_EMAIL_ADDRESS - your email; or whereever you want the zipped issue JSON files to be emailed to
- MAIL_USERNAME - Gmail account username
- MAIL_PASSWORD - Gmail token - guide: https://devanswers.co/create-application-specific-password-gmail/
- TOKEN - your GitHub PAT - doc: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

2. Create some sample issues, and run a test query to ensure it works ok.
- This workflow uses an action from the marketplace, so best to understand query capabilities directly from the source: https://github.com/marketplace/actions/query-issues-output

3. Manually launch the Action
- Visit the Actions tab
- Click on the action "Query Issues Output"
- "Run Workflow" from branch:main
- Wait a minute for a runner to pick it up and process the request (the time to run this workflow will depend on the number of issues matching the query)
- Check the email you set as "RECIPIENT_EMAIL_ADDRESS"


test

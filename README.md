# Find a LinkedIn profile from an email address

Find the LinkedIn profile attached to a work or personal email. This example reads a CSV of emails, runs **Email to LinkedIn Finder** on Apify, and saves the matched profile URL, name, headline, and company.

The code in this repository calls a published [Mawsool](https://mawsool.tech) Actor on [Apify](https://apify.com/oday). You use your own Apify token. The run is billed on Apify. Mawsool does not receive your CRM export, only the lookup you submit to the Actor.

**Start on Apify:** [Email to LinkedIn Finder](https://apify.com/oday/mawsool-email-linkedin-lookup)

**Talk to Mawsool:** info@mawsool.tech · osama@mawsool.tech · https://mawsool.tech

## How do I run it?

```bash
pip install -r requirements.txt
python enrich.py examples/input.csv --dry-run
set APIFY_TOKEN=your_apify_token
python enrich.py examples/input.csv --out results.json
```

On macOS or Linux, use `export APIFY_TOKEN=your_apify_token`.

Create the token at [Apify integrations](https://console.apify.com/settings/integrations). Replace `examples/input.csv` with your own list. The sample file uses example.com addresses so it is safe to commit.

## What does the CSV look like?

A header named `email` is required.

```csv
email
ada@example.com
grace@example.com
```

## What do I get back?

Each result row includes the input email, `hasLinkedIn`, `linkedinUrl`, `fullName`, `headline`, `company`, and `location` when a match exists. If the email has no confirmed profile, the row says so instead of guessing a different person.

## How much does it cost?

Email lookup is priced on the [Actor page](https://apify.com/oday/mawsool-email-linkedin-lookup). You pay for each email the Actor processes. The current price is always on the Actor page. Paid Apify plans receive the plan discount shown there.

`cost = rows processed × your plan price per row`.

## Which Mawsool Actor should I use?

- [Email to LinkedIn Finder](https://apify.com/oday/mawsool-email-linkedin-lookup)
- [LinkedIn Profile Finder by Name & Company](https://apify.com/oday/mawsool-linkedin-profile-finder)
- [LinkedIn Profile Details from URL](https://apify.com/oday/mawsool-linkedin-profile-details)
- [Mass LinkedIn Profile Scraper](https://apify.com/oday/mawsool-mass-linkedin-profile-scraper)
- [LinkedIn Current Company Checker](https://apify.com/oday/mawsool-linkedin-company-checker)
- [LinkedIn Job Change Detector](https://apify.com/oday/mawsool-linkedin-job-change-watch)
- [LinkedIn Company Details from URL](https://apify.com/oday/mawsool-linkedin-company-details)
- [Mass LinkedIn Company Scraper](https://apify.com/oday/mawsool-mass-linkedin-company-scraper)

## Related example clients

- [find-linkedin-profile-by-name](https://github.com/odayali1/find-linkedin-profile-by-name)
- [linkedin-job-change-checker](https://github.com/odayali1/linkedin-job-change-checker)
- [linkedin-company-enrichment](https://github.com/odayali1/linkedin-company-enrichment)

## Does this repository include Mawsool's data service?

No. This is an open-source example of how to start the public Actor and save the dataset. The Actor page is the product. For a data partnership, email info@mawsool.tech or osama@mawsool.tech.

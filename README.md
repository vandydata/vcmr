# VCMR standalone website

Authored on 2023-05-16

## Background

VGER's VCMR was previously hosted on Labnodes. It was transferred to FilemakerPro Server edition since that provided a WebDirect web hosting feature. We are now investigating simply hosting a simple CSV-based database of records with a simple HTML app via Github Pages.

## Features

1. Main page is “about VCMR” and table of all records. 
   a.	You can pick & choose which fields/columns to include. I tried to keep it succinct.
   b.	I intentionally avoided pagination. It is much easier/faster to scroll than click next page buttons
   c. A filter option exists to filter table rows by available `Type of Mutation`
2. Every record is linked to a page that only displays info about that record
   a.	URL is unique, so you can hyperlink to individual records
   b.	For now, I’m using the VGER ID in the URL, but we can do anything you’d like
   c.	I haven’t bothered with attachments yet
   d.	The record level data is being dumped into a table, just as a “demo” – we can/will style it up
   e.	Email/request details to be fine-tuned, etc…
3. Updating/adding records (for now, this is how I did it)
   a.	Took XLSX file you exported from FMPro
   b.	Opened in Excel, exported to CSV
   c.	Added to project repository (Github) and pushed to Github Pages
4. No “guest login” whatsoever
5. All front-end technology (html, javascript, css. all libs are CDN-provisioned)
   a.	HTML5
   b.	Bootstrap5
   c.	Jquery
   d.	Datatables


## Notes
- Data delivery

   - performed by Jennifer Skelton
   - Provides CSV and attachments (PDFs)

- IDE - webstorm
- local dev via local webserver - `python -m http.server 8000` then http://localhost:8000/index.html
- http://vcmr.vcscb.org/ - custom address, VUIT added CNAME record for DNS
- The `CNAME` file in the repository is Github-generated!
- HTTPS vs HTTP will take another ~24hrs until certificate is generated
- Hosting is via Github Pages, using “vcmr.vcscb.org” as custom domain:
- Requested for `vcmr` subdomain to be added as CNAME record via VUIT

   >  We would like to set up a subdomain for "vcmr.vcscb.org", via a CNAME record addition at the domain registrar:
   >
   >  subdomain: vcmr
   >  TTL: default is fine
   >  Target: vandydata.github.com

## Resources
- https://stackoverflow.com/questions/46455900/subdomain-of-website-for-github-pages-project 

## Releases

### 2025-02-12 - VCMRv8 (v 1.3)

- VCMRv7: 63 rows
- VCMRv8: 65 rows (+2 rows)

Number of columns:

- VCMRv7: 26 columns
- VCMRv8: 28 columns (+2 columns)

> Jennifer:
> Attached is version 8 of the VCMR. I have added two new columns, but that is just for my information. I have been working with the MGI to get strain names and strain MGI IDs for the lines we have in the repository. Those two columns (Strain MGI Allele Name & Strain MGI allele ID) do not have to be included in the data shown on the VCMR.

### 2025-06-27 - VCMRv9 (v 1.4)

- VCMRv9: 19 new rows
- Made the Primary citation (and primary citation 2) say “Not published” instead of Not provided

### 2025-11-04  - VCMRv11 (v 1.5)

- (skipped v10)
- VCMRv11: 1 new rows
- 

### 2026-04-30 - VCMRv12 (v 1.6)

- open xlsx, then export to CSV/UTF8 (not ANSI, as it drops special chars)

* Can this page be linked     back to the VCMR website? [https://medschool.vanderbilt.edu/vcmr/](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fmedschool.vanderbilt.edu%2Fvcmr%2F&data=05|02|jp.cartailler@Vanderbilt.Edu|c454945eeef642e6f93908dea6c26fd3|ba5a7f39e3be4ab3b45067fa80faecad|0|0|639131552449572614|Unknown|TWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D|0|||&sdata=6NjE0JZL5oDFQWmg%2BbDvWk78cn94Np2HDeaMmCc2oCU%3D&reserved=0)
* In the description at     the top of the page, the word “are” is missing. The Vanderbilt     Cryopreserved Mouse Repository (VCMR) contains a unique collection of     genetically-modified mice that ARE     available for rederivation.
* In the bullet point     section for accepting strains into the VCMR, please delete the word “to”     in the second bullet point. If the strain is available elsewhere,     has it been modified by changing the genetic background to through intercrossing with other alleles?
* When viewing several of     the strains or attachments, blocked or 404 errors occur. The page     may or may not load correctly when revisited. Any idea how to avoid     that?
* There are a few     attachments that did not load properly and one that needs to be removed,     listed below, so that I know I have attached them to this email. Plus, new     attachments for the new lines to be added:
  1. Add      Targeting_Map_ZI.pdf
  2. Remove under additional      information Genotyping_Protocol_XN.pdf
  3. Add      Genome_Editing_Strategy_YY.pdf
  4. Add      Genotyping_Protocol_AEU.pdf
  5. Add      Genome_Editing_Strategy_AEU.pdf
  6. Add      Genotyping_Protocol_AFF.pdf
  7. NEW:  Add      Genotyping_Protocol_ADV.pdf
  8. NEW:  Add      Genome_Editing_Strategy_ADV.pdf
  9. NEW:  Add      Genotyping_Protocol_ADW.pdf
  10. NEW:  Add      Genome_Editing_Strategy_ADW.pdf
  11. NEW:  Add      Genotyping_Protocol_ADX.pdf
  12. NEW:  Add      Genotyping_Protocol_AMY.pdf
  13. NEW:  Add      Genotyping_Protocol_AMX.pdf
  14. NEW:  Add      Genotyping_Protocol_AGC.pdf
  15. NEW:  Add      Genome_Editing_Strategy_AGC.pdf
  16. NEW:  Add      Genotyping_Protocol_AJA.pdf
  17. NEW: Add      Genome_Editing_AJA.pdf
  18. NEW: Add      Genotyping_Protocol_AMB.pdf


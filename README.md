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
   >  Target: vandydata.gith

## Resources
- https://stackoverflow.com/questions/46455900/subdomain-of-website-for-github-pages-project 

## Releases

### 2025-02-12 - VCMRv8

- VCMRv7: 63 rows
- VCMRv8: 65 rows (+2 rows)

Number of columns:

- VCMRv7: 26 columns
- VCMRv8: 28 columns (+2 columns)

> Jennifer:
> Attached is version 8 of the VCMR. I have added two new columns, but that is just for my information. I have been working with the MGI to get strain names and strain MGI IDs for the lines we have in the repository. Those two columns (Strain MGI Allele Name & Strain MGI allele ID) do not have to be included in the data shown on the VCMR.

### 2025-06-27 - VCMRv9

- VCMRv9: 19 new rows
- Made the Primary citation (and primary citation 2) say “Not published” instead of Not provided
- 


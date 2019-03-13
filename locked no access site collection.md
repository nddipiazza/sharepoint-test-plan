# 2.23 - locked no access site collection

## summary 

A site collection which was previously crawled is now "no accesS" locked. Recrawling the site collection should remove the corresponding indexed data.

## steps 1

  * Create site collection sc1 with site s1
  * Configure datasource with "fetch failure allowance =1" to allow deletion from index on recrawl
  * Crawl sc1 

## assertion 1 

  * Verify that sc1 and s1 items were crawled and indexed

## steps 2 (http://mstechtalk.com/sharepoint-how-to-lock-and-unlock-a-site-collection/)

  * In central admin console, edit sc1 and set to "no access"
  * Crawl sc1 using same datasource

## assertion 2

  * Verify that corresponding site collection sc1 index contents are removed.
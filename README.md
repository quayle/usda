# USDA National Nutrient Database for Standard Reference, Release 25

Original database (sr25.mdb/MS Access) was downloaded from:
https://www.ars.usda.gov/Services/docs.htm?docid=22771

Then it was converted using mdbtools and script from:
https://github.com/elcio/mdb2mysql

Converted file had every row in separate INSERT. After 24h of loading
data to database, I dumped it using mysqldump. Difference is that on
my 6-7 years old TOSHIBA notebook, I can DROP,CREATE&INSERT same data
in less than 5 minutes.

After loading data to database, columns had different lengths than
they were in documentation so I changed them appropriately.

Compressed using: tar czf sr25.tar.gz sr25.sql
Uncompress using: tar -xzvf sr25.tar.gz

After uncompressing sr25.sql size is about 61MB.

Version with added relations is under 'relations' branch.

# PyFracFocusCsvImport

## Synopsis
A Python 3 program that extracts comma-separated value (CSV) files originally sourced via download from FracFocus's download web page and transforms them as follows:
* Renames the columns to a convention more suitable for import into databases such as PostgreSQL, SQL Server and SQLite.
* After renaming, columns that are foreign keys between CSV files have the same names for consistency purposes, i.e. "apples to apples, oranges to oranges."
* Chemical toxicity columns, matched on the "cas_nbr" (Chemical Abstract Society Registry Number) column, are inserted into each row when a match occurs.
* Each original row is translated and split into four different CSV files:
  * "disclosures.csv"
  * "purposes.csv"
  * "ingredients.csv"
  * "ingredients_toxicities_flattened_numeric.csv"
* The preceding is done for the convenience of later loading into relational databases of the end-user's choice.

## Source Code Management
This project uses Git and GitFlow for its version control. The most advanced source code is to be found in the "develop" branch, with the "master" branch perhaps being somewhat behind but likely more stable. The author uses GitKraken as the GUI console to manage this project.

## Project Management
This project uses Glo, accessible via the GitKraken console, to manage the Kanban board that tracks this project.

## ToDo List
* Enable programmatic loading of SQLite database.
* Integrate chemical toxicities into SQLite database.
* Enable programmatic loading of PgSQL database.
* Integrate chemical toxicities into PgSQL database.
* Enable programmatic unzipping of the archive file downloaded from FracFocus's download web page.  
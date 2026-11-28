# D2C Commerce: India and North America

## What this is

This is a web page that shows a list of direct-to-consumer (D2C) and online shopping brands from India and North America.

You can:
- search for a brand by name, category, city and more
- filter the list by category, HQ city or headcount, and click a brand name to open its website
- click a brand to see everything the sheet says about it
- see charts and numbers on the Analytics tab
- read what each word means on the README tab, and where each fact came from on the Sources tab

The page does not keep any brand information inside itself. It reads everything from the two data files listed below. To change the information, you only change those files.

## What is in this project

| File | What it is |
|---|---|
| `index.html` | The web page itself. You normally never touch this. |
| `data-brands.csv` | All brands for every geography in one file (one row per brand). The Region column says which geography a brand belongs to. |
| `data-trends.csv` | The category trends for every geography in one file (one row per category, with a Region column). |
| `category-fixes.csv` | Optional. Moves a brand to a different category without touching the sheet (see below). |
| `README.md` | This file. |
| `NEXT-TIME-PROMPT.md` | Text you can give to a new Claude or Grok to keep improving this project. |
| `HOW-TO-PUBLISH.md` | Click-by-click steps to create a GitHub account, upload these files and get your live link. |

## Where the data came from

All the data came from one Google Sheet. Two of its tabs became the two data files:

| Google Sheet tab | Data file |
|---|---|
| D2C brands all regions | `data-brands.csv` |
| Category trends (all regions) | `data-trends.csv` |

The page makes one geography for every different word in the Region column, so a new geography needs no change to the page. Only the data files change.

Nothing was added, shortened or changed. Every row and every column from the sheet is in these files. The page shows the values exactly as they are written in the sheet.

## How to update the data later

You will do this every few months.

1. Open your Google Sheet and update it as usual.
2. Click the tab "D2C brands all regions", then **File**, **Download**, **Comma Separated Values (.csv)**. Rename the downloaded file to `data-brands.csv`.
3. Do the same for the tab "Category trends (all regions)" and rename it to `data-trends.csv`.
4. Upload the two files to GitHub (HOW-TO-PUBLISH.md, Part 7). Files with the same name replace the old ones.

The first row of each file must keep the column names exactly as they are. `data-brands.csv` starts with Region, Global S.No, Regional S.No, Brand, Category and so on. `data-trends.csv` starts with Region, Category, Trend, Summary, Brands in list, Source URL.

## Rules for the data files

If you break a rule, the page shows a red message that tells you which file has the problem.

- Keep the column names in the first row exactly as they are. Do not rename, remove or reorder them by accident. The brands files need these 17 columns: S.No, Brand, Category, Sub-category, Website domain, HQ city, Founded year, Short note, Headcount (approx), Product portfolio, Sales model, ERP signals, Signal source, Growth signal, Signal reason, Signal date, Signal source URL.
- The category trends files need these 5 columns: Category, Trend, Summary, Brands in list, Source URL.
- The first row is the column names. After that, one brand per row, with no empty rows in between.
- Do not merge cells in the sheet. Do not leave a column name blank.
- Growth signal must be one of these four words: Growing, Stable, Struggling, Unclear. Any other word is still shown as written. The page shows a note about this in the README tab.
- Keep the file names exactly as written, with small letters.
- Save as CSV in UTF-8. Google Sheets does this for you. If you use Excel, choose **Save As**, then **CSV UTF-8 (Comma delimited)**.

## If something looks wrong

- **A red message appears at the top.** Read it. It names the file and the problem. Usually a file name is wrong or a column name was changed.
- **The page is empty or says it cannot read its data.** You probably opened `index.html` by double-clicking it on your computer. That does not work. Open your GitHub Pages link instead.
- **You updated a file but the page looks the same.** Wait two minutes and refresh with Ctrl + Shift + R (Windows) or Cmd + Shift + R (Mac).
- **The numbers look wrong.** Open the CSV file in Google Sheets or Excel and check that the columns line up under the right names.

## If you lose access to Claude

Everything you need is in this project. To keep improving the page with a new AI:

1. Open `NEXT-TIME-PROMPT.md` and copy the text under the line.
2. Open a new chat with Claude or Grok and paste it.
3. Attach `index.html`, this `README.md`, all the `.csv` files and `category-fixes.csv`.

To set the page up from scratch on GitHub, follow `HOW-TO-PUBLISH.md`. Keep a spare copy of all the files on your computer or in Google Drive.

## Who can see this page

If you use a free GitHub account, your project and your live link are public. Anyone who has the link can open the page, and anyone who finds your project on GitHub can download the data files. Only put information here that you are happy for other people to see.

## Changing the words at the top

The first lines inside the `<script>` part of `index.html`, under the heading `SETTINGS`, hold the page title, the short description under it, the Google Sheet name and the data file names. If you rename a data file, change its name there too, or ask Claude to do it for you.

## Moving a brand to another category (category-fixes.csv)

If a brand is in the wrong category, you can fix it without editing the Google Sheet. Open `category-fixes.csv` and add a line with three things: the market (for example India or North America, written exactly as in the Geography drop-down), the exact brand name, and the category you want. The category must already exist in that market. Upload the file the same way as the others. The README tab of each geography has a "Data notes" section saying how many brands were moved, and no brand is ever removed. A line that does not match is ignored and listed in that section. The best long-term fix is still to correct the category in the Google Sheet and download the CSV files again.

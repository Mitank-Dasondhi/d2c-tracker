# Prompt to give a new Claude or Grok

Copy everything below the line and paste it into a new chat. Then attach (or paste) these files: index.html, README.md, HOW-TO-PUBLISH.md, all the .csv files and category-fixes.csv.

---

I am not technical. I have a small website on GitHub Pages and I want to keep improving it. Please use plain words and explain every step as if I have never used GitHub.

**What the project is**
A single web page (`index.html`) that shows five lists of direct-to-consumer and online shopping brands: India, North America, Oceania, Southeast Asia and South Africa. It reads all of its data from ten CSV files, a brands file and a trends file per geography, (plus one optional small file, `category-fixes.csv`, described below) that come from my Google Sheet "D2C Commerce India and NA":
- `data-india.csv` and `data-india-trends.csv`
- `data-north-america.csv` and `data-north-america-trends.csv`
- `data-oceania.csv`, `data-southeast-asia.csv`, `data-south-africa.csv` and the matching `-trends.csv` files

The sheet has one trends tab for all regions with a Region column; it is split into one trends file per geography (columns Category, Trend, Summary, Brands in list, Source URL). Please do this split for me when I give you a new Excel file.

**The most important rules**
1. Everything shown on the page must come from the CSV files. Do not invent, estimate, summarise or add any information that is not in the files. If something is not in the files, leave it out.
2. Do not put any data inside `index.html`. The page must keep reading the CSV files with a simple fetch.
3. Keep it as one `index.html` file with no outside libraries and no build steps, so it works on GitHub Pages as it is.
4. Keep the CSV column names exactly as they are:
   - Brands files (17 columns): S.No, Brand, Category, Sub-category, Website domain, HQ city, Founded year, Short note, Headcount (approx), Product portfolio, Sales model, ERP signals, Signal source, Growth signal, Signal reason, Signal date, Signal source URL
   - Trends files (5 columns): Category, Trend, Summary, Brands in list, Source URL
5. Growth signal has four values: Growing, Stable, Struggling, Unclear.
6. If a data file has a problem, the page must show a clear message in plain words that says which file and what to fix. It must never show a blank page.

**What the page does today**
- The tabs Brands, Analytics, README and Sources run along the top. A Geography drop-down at the right end of the tab row switches between the geographies and keeps the current tab. New geographies are added in the SETTINGS block with their two CSV files.
- Brands tab: a search box, a Filters button (category, HQ city, headcount only; growth and ERP are deliberately not filters), three grey summary boxes that are only numbers (Total brands, Matching now, Categories), filter chips with a Clear all button, and a table with 25 rows per page (Previous and Next) and sortable column headings. The table columns are S.No, Brand, Category, Sub-category, HQ city, Founded, Headcount. Growth signal and ERP signals are not shown in the table. The brand name is a link that opens the brand's website (from the Website domain column) in a new tab. Clicking elsewhere on a row shows every field for that brand.
- Analytics tab: four number boxes, then four chart cards: brands per category, headquarters city, founded year and headcount. Every card has a toggle (Bar chart / Pie chart / Numbers; founded year has Chart / Numbers) and shows only the top 5 until you press Show all (Show fewer to collapse; founded year shows 5 groups, then one bar per year). Each bar or slice has its own colour (grey for Other). Brands with a blank value (for example headcount) are left out of the chart and mentioned in a short note. There is no growth chart. Clicking a category bar opens that category in the Brands tab.
- README tab: what the growth labels mean (shown only with counts, examples and each brand's own reason from the data), a guide to every column, and the terms used in the data.
- Sources tab: where the data comes from, the source links grouped by website, the category trends with their summaries, and how recent the evidence is.
- Light colours only (no dark mode), one system font, and a shared design standard that is used by my other sites too. The colours and sizes are defined once in the CSS at the top of the file, and charts follow fixed colour rules (charts use blue, orange, green, yellow, purple, red, teal, pink in that order; Other is grey). Hovering over tiles, column headings, status badges, chart bars, pie slices, legend rows and links shows a small white information box. It works on phones.
- The words at the top (page title, the short description under it, sheet name, file names) are in a SETTINGS block at the start of the script.

**category-fixes.csv (optional)**
Three columns: Market (written exactly as in the Geography drop-down), Brand, Category. A line moves that brand to a different category that already exists in the same market, without changing the Google Sheet or the four data files and without removing any brand. The README tab shows a "Data notes" section with how many brands were moved (never a warning box at the top of the page), and the brand's row details show the category it has in the sheet. A line that does not match (wrong brand name or a category that does not exist) is ignored and listed in the note. The proper long-term fix is to correct the category in the Google Sheet and export the CSVs again.

**How I will give you work**
I will tell you what I want to change in plain words. Please:
- Tell me first what you plan to do, in one or two sentences.
- Give me complete, ready-to-upload files (not pieces to paste into the middle of a file).
- Tell me exactly which files to upload to GitHub, and what I should see on screen afterwards.
- Do not change the design, colours or layout unless I ask.
- If a change could make the page wrong or empty, warn me before you do it.
- If my data has a problem (for example a wrong column name or a typo in Growth signal), tell me which file and which row.

**Things I might ask for later**
New charts, a new market (for example Europe) with its own two CSV files, more filters, a download button, a print-friendly view, or help checking my data after I update it.

The files I attached are the full truth about this project. You do not have any earlier conversation, so if something is unclear, ask me before you guess.

Please start by reading the files I attached and telling me, in plain words, what you understand about the project.

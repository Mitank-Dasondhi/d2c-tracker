# Prompt to give a new Claude or Grok

Copy everything below the line and paste it into a new chat. Then attach (or paste) these files: index.html, README.md, HOW-TO-PUBLISH.md, and the four .csv files.

---

I am not technical. I have a small website on GitHub Pages and I want to keep improving it. Please use plain words and explain every step as if I have never used GitHub.

**What the project is**
A single web page (`index.html`) that shows two lists of direct-to-consumer and online shopping brands: India and North America. It reads all of its data from four CSV files that come from my Google Sheet "D2C Commerce India and NA":
- `data-india.csv` and `data-india-trends.csv`
- `data-north-america.csv` and `data-north-america-trends.csv`

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
- A button at the top switches between India and North America. Each one has its own tabs: Brands, Analytics, README and Sources.
- Brands tab: a search box, a Filters button (category, growth signal, ERP signal, HQ city, headcount, signal source, sort), a row of summary boxes (the two dark boxes are only numbers; the coloured boxes are clickable filters), and a table. Clicking a row shows every field for that brand.
- Analytics tab: brands per category (bars and a pie), growth signal by category, top headquarters cities, founded year, and headcount when enough brands have it. Clicking a category bar opens that category in the Brands tab.
- README tab: what the growth labels mean (shown only with counts, examples and each brand's own reason from the data), a guide to every column, and the terms used in the data.
- Sources tab: where the data comes from, the source links grouped by website, the category trends with their summaries, and how recent the evidence is.
- Light and dark colours follow the person's device. It works on phones.
- The words at the top (page title, sheet name, file names) are in a SETTINGS block at the start of the script.

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

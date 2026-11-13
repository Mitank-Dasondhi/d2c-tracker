# How to put this page on the internet (step by step)

This guide is for someone who has never used GitHub. GitHub sometimes changes the wording on its buttons, so a button may be named slightly differently from what is written here. The idea stays the same.

Here is the plan in plain words:
- You create a **GitHub account** for yourself.
- You create an **organization**. This is a shared home with one name. Every bot you build will live under it.
- Inside the organization, each bot gets its own **repository**. A repository is a folder of files for one bot. This D2C page will be the first one.

Free GitHub Pages needs a Public repository. That means anyone with your link can open the page, and anyone who finds the repository on GitHub can download its files. Only put information here that you are happy for others to see.

## Part 1: Create your GitHub account

1. Open github.com in your browser. You will see a **Sign up** button in the top-right corner. Click it.
2. Enter your email, a password and a username. You will see a puzzle to prove you are a person. Solve it.
3. Click **Create account**. GitHub emails you a code. Open your email, then type the code into the GitHub page.
4. GitHub may ask a few questions about you. You can skip them. If it asks you to choose a plan, choose the **Free** one. You should now see your GitHub home page with your username at the top-right.

## Part 2: Create the organization (the shared home)

5. Click the **+** icon in the top-right corner, then click **New organization**. You will see a page asking you to choose a plan.
6. Choose the **Free** plan.
7. Fill in the form:
   - **Organization name:** choose something short, in small letters, with no spaces. This name becomes part of every live link, for example `yourorg.github.io/vc-list`. It is hard to change later without breaking links, so think before you click.
   - **Contact email:** your email.
   - **This organization belongs to:** choose **My personal account**.
   Click **Next**. You may see another puzzle.
8. If it asks you to invite people, skip that step. You should now see the page of your organization, with its name at the top and an empty list of repositories.

Tip for later: protect yourself from losing access. Add a second owner you trust. In the organization, click **People**, then **Invite member**, and give them the **Owner** role.

## Part 3: Create the first repository (this D2C page)

9. On your organization's page, click the green **New repository** button. If you do not see it, click the **+** icon in the top-right and choose **New repository**.
10. In the **Owner** box, make sure your organization is selected, not your personal username.
11. In **Repository name**, type a short name with no spaces, for example `vc-list`. This also becomes part of your link.
12. Choose **Public**. Leave all the other boxes empty. Do not tick "Add a README file". Click the green **Create repository** button. You will see a page titled "Quick setup" with several grey boxes of text.

## Part 4: Upload your files

13. On that page, find the sentence "Get started by creating a new file or uploading an existing file". Click the blue words **uploading an existing file**. You will see a big dotted box that says "Drag files here".
14. Open the folder on your computer where you saved the project files. Select all the files: `index.html`, the four `.csv` files, `README.md`, `NEXT-TIME-PROMPT.md` and `HOW-TO-PUBLISH.md`. Drag them into the dotted box. You can also click **choose your files** and select them.
15. Wait until every file is listed on the page, each with a small progress bar that finishes. Drag in the files only, not a folder.
16. Scroll to the bottom. Click the green **Commit changes** button. Committing just means saving. You will see your repository page again, now listing all the files.

## Part 5: Turn on your live page

17. Near the top of the repository page, click **Settings** (it has a small gear icon). If you do not see it, click the **...** menu next to the tabs.
18. In the left menu, click **Pages**. You will see a section called "Build and deployment".
19. Under **Source**, choose **Deploy from a branch**. Under **Branch**, click the drop-down that says "None" and choose **main**. Leave the folder as **/ (root)**. Click **Save**.
20. Wait one to two minutes, then refresh the page (press F5). You should see a box at the top that says "Your site is live at" followed by a link like `https://yourorg.github.io/vc-list/`. Click **Visit site**.

## Part 6: Check it works

21. Your page opens in a new tab. You should see the title "D2C Commerce India and NA" and two round buttons, **India** and **North America**, each with a number. Below them are the tabs Brands, Analytics, README and Sources, then a search box and a table of brands.
22. Click **North America**, then type a brand name into the search box. The table should shrink to match.
23. If you see a red box, read the message. It names the file and the problem, and README.md explains how to fix it. If you see a plain "404" page, wait another two minutes and try again.
24. Bookmark the link. To find it again later, go to your repository, click Settings, then Pages.

Do not open `index.html` by double-clicking it on your computer. Browsers block it from reading the data files that way, and the page will tell you so. Always use your GitHub Pages link.

## Part 7: Update the data later

25. Update your Google Sheet. Click the tab you changed, then click **File**, **Download**, **Comma Separated Values (.csv)**. This downloads only the tab you are looking at.
26. Rename the downloaded file to its exact name:
    - Brands tab: `data-india.csv`
    - Category trends tab: `data-india-trends.csv`
    - Brands - North America tab: `data-north-america.csv`
    - Category trends - NA tab: `data-north-america-trends.csv`
27. Go to your repository on GitHub. Click **Add file**, then **Upload files**. Drag in the new CSV files. Files with the same name replace the old ones.
28. Click the green **Commit changes** button. Wait one to two minutes, then open your live link and press Ctrl + Shift + R (Windows) or Cmd + Shift + R (Mac). You should see the new numbers on the India and North America buttons.

## Part 8: Add another bot later

Every new bot gets its own repository inside the same organization.

29. Go to your organization's page and click **New repository**. Check that the **Owner** box shows your organization.
30. Give it a new short name, for example `news-bot`. Choose **Public**, and click **Create repository**.
31. Upload that bot's files the same way as in Part 4, then turn on the live page the same way as in Part 5.
32. Its link will be `https://yourorg.github.io/news-bot/`. Your D2C page keeps working at its own link and is not touched.

If a bot holds private information, do not put it in a Public repository. The free version of GitHub Pages cannot keep a page private.

## Part 9: Get help improving a page later

Open a new chat with Claude or Grok. Open the file `NEXT-TIME-PROMPT.md` in the repository, copy the text under the line, paste it into the chat, and attach `index.html`, `README.md` and the four `.csv` files. The AI will then understand the whole project without needing any earlier conversation.

Keep a copy of all these files somewhere else too, for example in a folder on your computer or in Google Drive. Then you can always rebuild the project even if you lose access to your GitHub account.

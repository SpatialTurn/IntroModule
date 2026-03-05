---
title: "How to Create Your Own Carpentries-Style Workshop Website Using GitHub"
teaching: 40
exercises: 20
---

# How to Create Your Own Carpentries-Style Workshop Website Using GitHub

**A beginner-friendly guide for instructors, lesson authors, and community members**

After this lesson you will be able to:

- Create a professional-looking workshop website using The Carpentries template
- Host it for free on GitHub Pages
- Customize key information (dates, instructors, setup instructions)
- Understand why we avoid forking and use the template instead

**Target audience**: Anyone planning a Carpentries-style workshop (Software, Data, Library Carpentry) who has a basic GitHub account.

**Prerequisites**:
- A free GitHub account (sign up at github.com if you don't have one)
- A web browser
- (Optional but recommended) Basic familiarity with Markdown

---

## Why Use The Carpentries Workshop Template?

The Carpentries provides a ready-made template that:

- Looks professional and consistent with hundreds of Carpentries workshops
- Automatically generates schedule, setup, FAQ, and other standard pages
- Is mobile-friendly
- Is hosted for free via **GitHub Pages**
- Supports easy customization via one main file (`_config.yml`)

There are two main Carpentries website types:

- **Workshop websites** → short-term event pages (what this guide covers)
- **Lesson websites** → long-term curriculum pages (uses The Carpentries Workbench — see notes at end)

---

## Step 1: Create Your Repository from the Template

**Important**: Do **NOT** fork the repository — use GitHub's "Use this template" feature instead.

1. Go to:  
   https://github.com/carpentries/workshop-template

2. Click the green **Use this template** button (top right) → **Create a new repository**

3. Fill in the details:
   - **Owner**: your GitHub username or an organization
   - **Repository name**: Use the Carpentries naming convention:  
     `YYYY-MM-DD-sitename-lessonname`  
     Example: `2026-05-15-purdue-python-novice`
   - Description (optional): "Python for Beginners – May 2026, Purdue University"
   - Visibility: **Public** (required for GitHub Pages)

4. Click **Create repository**

> **Tip**: If you forget the naming convention, your site will still work — but using the slug format helps The Carpentries index your workshop.

---

## Step 2: Install GitHub Desktop.

1. After installation, login to the application. 

2. Click on `File` then `Clone Repository` on the top left. 

3. Find the newly created repository and save it locally on your desktop. 

4. Go the folder which has the cloned repository. 

5. Any change you make in this folder will reflect on the GitHub desktop application. Make sure to **save** the changes.

6. After making the changes, add a summary (this is required), and then `Push` on the top right of the application. 

That's it! Now you can make changes locally to your webpage without having to open GitHub in a browser.  

**Tip:** If you happen to make changes to the webpage repository from a browser and to make sure you have saved the progress locally in your desktop, all you have to do is `Fetch Origin` in the top right of the application to update your local folder repo of the changes. 

## Step 3: Enable GitHub Pages  - Create another repository 

GitHub Pages builds and hosts your site automatically from the `gh-pages` branch.

1. In your new repository, go to **Settings** (top tab)

2. Scroll down to **Pages** (in the left sidebar, under "Code and automation")

3. Under **Source**:
   - Branch: select `gh-pages`
   - Folder: select `/ (root)`
   - Click **Save**

4. Wait 1–2 minutes, then refresh.  
   GitHub will show:  
   "Your site is live at https://**your-username**.github.io/**your-repo-name**/"

Copy this URL — that's your website!

5. In our case, we have a repository/webpage name called `spatialturn.github.io`. See [here](https://github.com/SpatialTurn).

---

## Step 4: Edit the Main Configuration File (`_config.yml`)

This single file controls almost everything.

1. In your repository, open the file called `_config.yml`

2. Edit these key fields (use the pencil icon → commit changes):

```yaml
# --- general ---
title: "Python for Novices"                     # Workshop title
life_cycle: "upcoming"                          # or past/current
carpentry: "dc"                                 # dc = Data Carpentry, swc = Software, lc = Library
country: "us"                                   # two-letter code
country-full: "United States"
city: "West Lafayette"
venue: "Purdue University, Wilmeth Active Learning Center"
address: "155 S Grant St, West Lafayette, IN 47907"
contact: "instructor@purdue.edu"
handout: ""                                     # optional link to Etherpad/Google Doc
eventbrite: ""                                  # optional registration link

# --- dates ---
start_date: "2026-05-15"
end_date: "2026-05-16"

# --- instructors/helpers ---
instructor:
  - Jane Doe
helper:
  - Helper Name One
  - Helper Name Two

# --- links ---
website: ""                                     # leave blank — GitHub fills it


3. Create a file called `index.html` or whatever name you prefer. This will be the place where you make changes to your webpage.

---

## Final Step  - Adding Content to Webpage. 


1. Open the folder called episodes in repository created using the carpentry template in Step 1. 

2. You should see a file called `introduction.md`. 

3. This is the file where you can add content for a specific module. 

4. You can always add newer modules by adding newer .md or markdown files within the episodes folder. 

5. Make sure to add that particular file name in `config.yaml` file and save it. It is usually around line 67.  

6. By default `config.yaml` has only `introduction.md` but you can more to that if you decide to add more content to it. 

7. Check the changes we made when we created our webpages for the Data Analysis module [here](https://github.com/SpatialTurn/DataAnalysis).  

**Tip:** See the changes we made to `episodes` folder and `config.yaml` file. 


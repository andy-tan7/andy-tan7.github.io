# Hosting your Resume on GitHub Pages: A Guide

## Purpose
This readme will guide a user on the process of hosting their resume on GitHub Pages. The documentation here will serve to guide completely new users as well as provide a refresher for experienced users. Here, you will find ways to convert your resume into Markdown format, learn how to upload it to GitHub Pages, and apply a theme with Jekyll.  

### Technical Writing
This document is inspired by Andrew Etter's book, [Modern Technical Writing]. Etter suggests making static websites to utilize their speed, simplicty, portability, and security. For resumes, you'll find that keeping them up to date after sending them out is a challenge, and hosting them as static webpages is an easy solution to this problem. The following guide will demonstrate how simple it is to host your resume as a static webpage.

## Prerequisites

This guide assumes that you have access to a web browser; it will not be using any command line interfaces (e.g., Git).  
Our technology stack will be Visual Studio Code as the text editor, GitHub Pages as the host, and Jekyll as our static site generator.

* Text Editor: Visual Studio Code
* Host: GitHub Pages
* Static Site Generator: Jekyll


### Visual Studio Code
* We will be using [Visual Studio Code] as a text editor for the markdown-formatted resume. While you can use whichever markdown editor you prefer, this tutorial will reference features that exist in VS Code. 

  * The instructions in this guide will not teach markdown syntax or formatting. You can find out how to write in markdown format [here](#more-resources). 

### GitHub Pages
* You will need to create an account on [GitHub] for this project. If you already have an account, you can use your existing one.
* Don't worry about downloading anything for Jekyll for now. This will be covered later in the tutorial.

## Tutorial
### Create your markdown resume
1. Open Visual Studio Code.
2. Create a new file. 
    * This can be done via **File → New File** in the top left corner, or by using the **Ctrl+N** hotkey.
3. Save this file as **"index.md"**. This will come in handy later when uploading to GitHub.
4. Complete your markdown resume. See [more resources](#more-resources) for more of a guide on how to do this.
    * Tip: you can preview your markdown file while editing it in VS Code by clicking on the _Open Preview to the Side_ button in the top right corner of the editor. To use the keyboard shortcut for this, press Ctrl+K, release Ctrl, and press V.  
> Note: you may want to avoid using tables in markdown; you may find that the Jekyll themes we use later do not properly support markdown tables. 

### Upload your content to GitHub
1. Create a new GitHub repository.
    * Log into GitHub. Click the plus (+) icon on the right side of the site banner (next to your profile badge) on any page. This will open a drop-down with **New Repository** as one of the options. The next page will prompt you to enter some information.
      * For the *repository name*, we will want to use **andy-tan7.github.io**, where you can replace my ID with your GitHub ID.
      * Make sure your repository is set to **Public**, rather than Private.
      * Optionally, you may include a description and a README file. We will leave everything else on their default settings for now.
      * When you're ready, click the **Create repository** button at the bottom of the page.
![Create repository screenshot]

At this point, you will be taken to the **Code** tab in your new repository.

2. Upload your resume file.
    * If you did not add a README file, click on __*uploading an existing file*__ in the blue *Quick setup* box.
        > Note: If you created the project with a README file, you can click on the **Add file** button and select *Upload files*.
    * Drag your index.md resume file into the indicated area or browse for your file manually from there.
    * Optionally, you can write a description for the change you are about to commit.
    * Once you're ready, click the **Commit changes** button to confirm your upload.

From here, you should have a repository with an index.md file (and a readme if you chose to include one).

### Add a theme for your resume with Jekyll.

1. Go to the Settings tab in your repository.
    * This will be the rightmost tab under your project banner at the top.
2. Find the **Pages** category in the list on the left side of the settings menu.
3. In the **Theme Chooser** section, click the **Choose a theme** button.
    * Browse through the themes at the top until you see one that you like. Each theme will show a sample preview underneath when selected.
    * I used the *Slate* theme for my own resume, which provides a clean and appealing look.
    * Once you're satisfied with your choice, click the **Select theme** button to confirm your selection.

At this point, you will be taken back to the Settings page, and GitHub Pages will automatically publish your site for you. You can click the link in the green box in the Settings → Pages menu to preview it.

![Your site is published screenshot]
> Note: it will often take several minutes for your changes to be applied. Don't be alarmed if it seems like nothing happened when you submit changes. Simply wait a few minutes and refresh the page, and then you should see your changes.

### Set a proper title for your resume
You will notice that the title at the top of the page is currently the name of your repository. Let's fix this.

1. Navigate back to the **Code** tab in your repository.
    * There should now be a _config.yml file in your file list. Click this file, and then click the pencil icon on the right to edit it.  
    ![Edit this file]
    * We will want to add a *title* line. I used my name as the title. Add a line like ```title: Andy Tan``` to the end of the file, where you can replace my name with the title you want for your resume.
2. You may optionally provide a description of the change you are about to commit. Once you are ready, press the green **Commit changes** button at the bottom of the page.

And with that, your resume is hosted on GitHub pages!  

![Done gif]

## More Resources
Here are some extra links to support your markdown writing process if needed.
* Markdown beginner tutorial: <https://www.markdowntutorial.com/>
* Markdown quick reference: <https://www.markdownguide.org/cheat-sheet/>
* Extended markdown syntax: <https://www.markdownguide.org/extended-syntax/>
* Andrew Etter's book, [Modern Technical Writing]. 

## Authors and Acknowledgements
Credit to me (Andy Tan) for writing this article, and to the various contributors of the [Slate] Jekyll theme. Also, special thanks to my peers in Group 7 for providing peer review: Faith de Leon, Michael Bathie, Koye Fatoki, and Tuan Le.

## FAQ

* Why is Markdown better than a word processor?
  * Markdown uses a clean and universal syntax, compatible with many static site generators to host your page using various templates and styles. This can help you create a simple and portable online resume.
* Why are my theme changes and resume edits not being published?
  * GitHub often takes a few minutes to apply your changes. Simply wait a couple minutes and then refresh the page, and your change should appear. 

[Visual Studio Code]: https://code.visualstudio.com/download
[GitHub]: https://github.com/join
[Slate]: https://github.com/pages-themes/slate
[Modern Technical Writing]: https://www.goodreads.com/book/show/28433138-modern-technical-writing

[Create repository screenshot]: images/create_repository.png "New repository settings"
[Your site is published screenshot]: images/site_published.png "Your site is published at..."
[Edit this file]: images/edit_file.png "Edit file button"
[Done gif]: images/done.gif "All done!"

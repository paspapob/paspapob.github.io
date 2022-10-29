

# Hosting a Markdown resume with GitHub Pages and Jekyll on Windows

<img src="./img/hostedres.gif" width="745">

## 👋 Introduction and Purpose

This documentation provides the instructions and tools necessary to host a
Markdown formatted resume on Windows using **Markdown, Atom, GitHub Pages,
and Jekyll.**

### Software stack explanation
Markdown
- Markdown is a lightweight markup language that is used to format
plaintext documents.
- Elements of Markdown are used to format text into headings,
lists, and more.

Atom
- A free and open-source text editor, which can be used to edit Markdown files

GitHub Pages
- Static site hosting service that turns GitHub repositories into a websites
- This will be used to host a Markdown formatted resume

Jekyll
- A static site generator which will be used to convert plain text files into a
static website
- Jekyll is necessary to generate the site that will be hosted by GitHub Pages

### *Why should someone host a website and Markdown resume?*
Having a personal website is a great way to connect with others. Hosting a
website with GitHub Pages creates an avenue for others to view content.
This could be resumes, projects, portfolios, media, and much more.
Hosting a resume in Markdown allows users to view your resume from different
platforms and devices. For example, Markdown can be created and viewed using
the most common (and uncommon) operating systems. Moreover, technological
advancements will not impede the utility of Markdown as it can be read using
a simple text editor. This results in a document that can be hosted and shared
indefinitely without concern for incompatibility.


## ✏️ Getting started

To get started, the following tools must be installed/set-up.

### Markdown
Prepare and complete a Markdown formatted resume. Markdown files can be created
and edited using Atom. This resume will be hosted on the completed site.

### GitHub
As the hosted resume will be hosted using GitHub Pages, it is necessary to own
a GitHub account. Registration for GitHub can be done by visiting the following
link: https://github.com/join

### Git
Git is software used for distributed version control, in this case we will be
using Git to manage and work with repositories.

Install Git by downloading the appropriate installation package from your
system. This can be done by going to the following link:
 https://git-scm.com/download/win

During installation, **ensure that you enable Git to be used from the
Command Prompt/Command line**.


### GitHub Desktop
GitHub Desktop is software utilizing a GUI to implement Git.

GitHub Desktop can be downloaded and installed at the following
link: https://desktop.github.com/

### Jekyll
Jekyll is based on **Ruby**. Consequently, Ruby must be installed as a
prerequisite before using Jekyll.

Instructions on how to install Ruby on Windows can be found on the
official Jekyll website at https://jekyllrb.com/docs/installation/windows/

Confirm that Jekyll has been properly installed by opening Command Prompt
and running command `jekyll -v`




## 🛠 Installation

### *Step 1: Create a GitHub Repository*

A GitHub repository will be used to contain the files necessary to host
the website.

Create a Github repository by first opening Github.com while logged into your
created Github account.

1. Click the + drop-down menu in the upper right corner of the page and
select **New repository**
2. Enter USERNAME.github.io into the "Repository name" input box, **such that
USERNAME is the username associated with the GitHub account**.
3. At the bottom of the page, click **"Create Repository"**.
4. Take note of the URL of the repository page in order to proceed with Step 2.

>❗️
>From Step 2 onwards, USERNAME will be used as a place holder for the username
associated with the created GitHub Account

### *Step 2: Clone a repository for local use*

A local version of the repository is needed to generate a static site using
Jekyll. Before proceeding, open GitHub Desktop and sign in with the account
created in Step 1.


1. Navigate to the URL of the repository page created in Step 1.
2.  Under Quick setup, click "Set up in Desktop" and follow the instructions
provided. Note the local path chosen for the local repository.



### *Step 3: Generate and setup a static site using Jekyll*

Following Step 2, Jekyll can now be utilized to generate the files necessary
for a static site.

1. Open Command Prompt and change directory to the local path noted in Step 1.
2. Create a new Jekyll site by running the command "jekyll new --skip-bundle ."
3. Open the Gemfile that Jekyll created within the local path.
4. Add "#" to the beginning of the line that starts with `gem "jekyll"`
5. Replace the line starting with `# gem "github-pages"` with the
following line:
<br> `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins`
such that **GITHUB-PAGES-VERSION** is the latest supported version of the
github-pages gem. The latest supported version can be found at the
following link: https://pages.github.com/versions/
<br> For example, the replacing line for github-pages version 227 would
be `gem "github-pages", "~> 227", group: :jekyll_plugins`
6. Save and close the Gemfile.
7. Run the command `bundle install` from the Command Prompt.
8. Commit the changes to your local repository by opening GitHub Desktop and
clicking "Commit to Main" with a summary description, then
click "publish branch"
9. Confirm the site has been generated by opening
USERNAME.github.io in the browser.

### *Step 4: Host the Markdown Resume*
1. Copy and paste the Markdown formatted resume into the root of
the local path.
2. Rename the file to "resume.md"
3. Open resume.md in Atom and add the following code to the top of the
file. <br>  `---` <br> `layout: page`
`title: "Resume"`
`permalink: /resume`
`---`
5. Commit and publish the changes in GitHub Desktop.
6. Confirm the Markdown formatted resume has been hosted
by opening USERNAME.github.io/resume in the browser


## Configuration

### Flags



### Environment variables



## Third-party integrations

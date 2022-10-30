

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
- Markdown will be used to utilize syntax elements such as headings,
lists, and more.

Atom
- A free and open-source text editor, which can be used to edit Markdown files.

GitHub Pages
- Static site hosting service that turns GitHub repositories into a websites.
- This will be used to host a Markdown formatted resume.

Jekyll
- A static site generator which will be used to convert plain text files into a
static website.
- Jekyll is necessary to generate the site that will be hosted by GitHub Pages.

### *Why should someone host a website and a Markdown resume?*
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

```
For Step 1, Etter's principle of avoiding formal documentation
(unnecessary information and repetition) must be utilized to ensure readers
are not encouraged to skim through instructions. To implement this, each task
in Step 1 is succinct.
```

### *Step 1: Create a GitHub Repository*

A GitHub repository will be used to contain the files necessary to host
the website.

Create a Github repository by first opening Github.com while logged into your
created Github account.

1. Click the + drop-down menu in the upper right corner of the page and
select **New repository**
2. Enter USERNAME.github.io into the "Repository name" input box, **such that
USERNAME is the username associated with the GitHub account**.
3. Click **"Create Repository"** located at the bottom of the page.

>❗️
>From Step 2 onwards, USERNAME will be used as a place holder for the username
associated with the created GitHub Account

```
The note implemented above is also another aspect of avoiding
formal documentation, using a note to reduce repetitive text.
```

```
Step 2 adheres to Etter's rule of writing using the minimum possible length.
In the tasks below, the context provided is only that of what is necessary.
For example, the description of Step 2 states that the user needs to sign into
GitHub Desktop. There is no further additional information detailing the
additional uses of GitHub Desktop as it is unnecessary for this step.
```

### *Step 2: Clone a repository for local use*

A local version of the repository is needed to generate a static site using
Jekyll. Before proceeding, open GitHub Desktop and sign in with the account
created in Step 1.


1. Navigate to the URL of the repository page created in Step 1.
2. Click "Set up in Desktop" in the Quick setup section
3. Provide an appropriate local path for the repository and select "Clone"

```
In Step 3, there are multiple tasks that involve shell commands. Etter
recommends that instead of writing from memory, it is better to copy and paste
the commands after validating that they work. This is in contrast to
broadly explaining what kind of shell command should be used.
In the tasks provided, shell commands can be directly copied and pasted
from the instructions into the Command Prompt.
```

### *Step 3: Generate and setup a static site using Jekyll*

Following Step 2, Jekyll can now be utilized to generate the files necessary
for a static site. Before proceeding, note the latest supported version of
github-pages, which can be found at the following
link: https://pages.github.com/versions/

1. Open Command Prompt and change directory to the cloned repository
2. Run the command "jekyll new --skip-bundle ."
3. Open the newly generated Gemfile with Atom.
4. Add "#" to the beginning of the line that starts with `gem "jekyll"`
5. Replace the line starting with `# gem "github-pages"` with the
following line:
<br> `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins`
such that **GITHUB-PAGES-VERSION** is the latest supported version of the
github-pages gem.
6. Save the Gemfile.
7. Run the command `bundle install` from the Command Prompt.
8. Open GitHub Desktop and provide a commit title.
9. Click "Commit to Main"
10. Click "Publish branch"
11. Confirm the site has been generated by opening
USERNAME.github.io in the browser.

```
Etter states that consistency is important as it makes writing appear more
approachable and easier to scan. The concept of consistency was implemented by
ensuring that each step is identical in composition. Each step has a short
description, followed by smaller tasks organized as a list.
```

### *Step 4: Host the Markdown Resume*

With the necessary files now generated, it is possible to host the Markdown
formatted resume.

1. Copy and paste the Markdown formatted resume into the root of
the local path.
2. Rename the file to "resume.md"
3. Open resume.md in Atom and add the following code to the top of the
file. <br>  `---` <br> `layout: page`
<br> `title: "Resume"`
<br> `permalink: /resume`
<br>`---`
5. Commit and publish the changes in GitHub Desktop.
6. Confirm the Markdown formatted resume has been hosted
by opening USERNAME.github.io/resume in the browser

### *More Resources*



[Markdown Tutorial](https://www.markdowntutorial.com/)
- Interactive tutorial for learning how to format text in Markdown

[Modern Technical Writing: An Introduction to Software Documentation](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- Excellent resource for learning how to create software documentation

[Awesome README](https://github.com/matiassingers/awesome-readme)
- GitHub hosted resource containing a curated list of high quality READMEs

## Authors and Acknowledgements
Lu, Junyi - LUJ8 <br>
Kolton, Zac - KOLTONZ <br>
Paspaporn, Benjamin - PASPAPOB <br>
Murray, Evan - MURRAYE2


## FAQs



### Why is Markdown better than a word processor?

As previously stated in the introduction, Markdown is easy to use and has a
small barrier to entry. Firstly, Markdown files can be made from any text editor
and can be utilized by users without a technical background. Secondly, Markdown
is incredibly versatile. Markdown can be read before it is formatted, and is
compatible with virtually all platforms and operating systems. In comparison to
Microsoft Word, Markdown does not require the use of a GUI to implement
elements such as headers, lists, tables, and more. Further, it can be easily
exported as a PDF, EPUB, HTML as Markdown is essentially plain text.

### Why is Windows not recognizing the "jekyll" command?

It is important to remember that following the completion of the Ruby
installation, users must open a new Command Prompt and install Jekyll by
running `gem install jekyll bundler`. Following this command, users can confirm
installation by running `jekyll -v`

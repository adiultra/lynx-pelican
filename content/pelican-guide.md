Title: Setting Up Pelican
Date: 2016-02-06 13:20
Category: web
Tags: blog, pelican


# How to setup Pelican

This a the setup of pelican, the static blog creator, which converts markdown to static html pages.

First off, Pelican is a command line tool, But don't scream, its perfectly sane and doesn't require your ninja skills to do cool stuff.

## 1. Installing Pelican

You can follow the official [guide]() to setup Pelican. Here I Show the steps to install it for linux.

Pelican can be easily installed if you have Python Installed, since python comes with pip (The package manager for python).

```bash
sudo -H pip install Markdown
sudo -H pip install pelican
```

> The 1st line installs markdown package for conversion from MD to HTML.

> Here `sudo -H` installs pelican (and Markdown) for all users, remove this to install for only the current user, that is you.

Now, when pelican is installed. We can move on to create the very first blog.

## 2. Pelican Quick Start

As the header says, let's run the `pelican-quickstart` Command.

> Replace path/to/yoursite with the path of the folder where you want pelican to reside

```bash
mkdir -p ~/path/to/yoursite
#optional if you already created a folder with your file manager

cd ~/path/to/yoursite
# this changes the directory to your folder

pelican-quickstart
# answer the questions asked and you get your site ready
```

Here is a sample setup :

```bash
adiultra@adiultra:~$ mkdir -p ~/Projects/pelicus
adiultra@adiultra:~$ cd ~/Projects/pelicus
adiultra@adiultra:~/Projects/pelicus$ pelican-quickstart
Welcome to pelican-quickstart v3.6.3.

This script will help you create a new Pelican-based website.

Please answer the following questions so this script can generate the files
needed by Pelican.


> Where do you want to create your new web site? [.]
> What will be the title of this web site? Pelicus
> Who will be the author of this web site? Aditya Cool
> What will be the default language of this web site? [en]
> Do you want to specify a URL prefix? e.g., http://example.com   (Y/n) n
> Do you want to enable article pagination? (Y/n) Y
> How many articles per page do you want? [10]
> What is your time zone? [Europe/Paris]  	Asia/Calcutta
> Do you want to generate a Fabfile/Makefile to automate generation and publishing? (Y/n) Y
> Do you want an auto-reload & simpleHTTP script to assist with theme and site development? (Y/n) Y
> Do you want to upload your website using FTP? (y/N) N
> Do you want to upload your website using SSH? (y/N) N
> Do you want to upload your website using Dropbox? (y/N) N
> Do you want to upload your website using S3? (y/N) N
> Do you want to upload your website using Rackspace Cloud Files? (y/N) N
> Do you want to upload your website using GitHub Pages? (y/N) y
> Is this your personal page (username.github.io)? (y/N) N
Done. Your new project is available at /home/adiultra/Projects/pelicus
```

Wow you have your Blog ready, but wait how do you add content? Read ON.

## 3. Writing Articles

In your blog there will be A folder named `content`. Since you created a new blog, It's empty, Don't worry. You will fill it very soon.

In this folder create a file named whatever you like (My-first-article.md is a great name) (Remember to add `.md` to your filename since this tells it that it is markdown).

Open it in your favorite text editor, I recommend [Atom](http://atom.io) for this job since it has excellent markdown support with live preview.

Add the following content to your file :

```markdown
Title: MarkDown Exhibit
Date: 2015-12-06 13:20
Category: Markus
Tags: blog, pelican

# An exhibit of Markdown

This note demonstrates some of what [Markdown][1] is capable of doing.

## Basic formatting

Paragraphs can be written like so. A paragraph is the basic block of Markdown. A paragraph is what text will turn into when there is no reason it should become anything else.

Paragraphs must be separated by a blank line. Basic formatting of *italics* and **bold** is supported. This *can be **nested** like* so.

## Lists

### Ordered list

1. Item 1
2. A second item
3. Number 3
4. Ⅳ

*Note: the fourth item uses the Unicode character for [Roman numeral four][2].*

### Unordered list

* An item
* Another item
* Yet another item
* And there's more...

## Paragraph modifiers

### Code block

    Code blocks are very useful for developers and other people who look at code or other things that are written in plain text. As you can see, it uses a fixed-width font.

You can also make `inline code` to add code into other things.

### Quote

> Here is a quote. What this is should be self explanatory. Quotes are automatically indented when they are used.

## Headings

There are six levels of headings. They correspond with the six levels of HTML headings. You've probably noticed them already in the page. Each level down uses one more hash character.

### Headings *can* also contain **formatting**

### They can even contain `inline code`

Of course, demonstrating what headings look like messes up the structure of the page.

I don't recommend using more than three or four levels of headings here, because, when you're smallest heading isn't too small, and you're largest heading isn't too big, and you want each size up to look noticeably larger and more important, there there are only so many sizes that you can use.

## URLs

URLs can be made in a handful of ways:

* A named link to [MarkItDown][3]. The easiest way to do these is to select what you want to make a link and hit `Ctrl+L`.
* Another named link to [MarkItDown](http://www.markitdown.net/)
* Sometimes you just want a URL like <http://www.markitdown.net/>.

## Horizontal rule

A horizontal rule is a line that goes across the middle of the page.

---

It's sometimes handy for breaking things up.

## Images

Markdown can also contain images. I'll need to add something here sometime.

## Finally

There's actually a lot more to Markdown than this. See the official [introduction][4] and [syntax][5] for more information. However, be aware that this is not using the official implementation, and this might work subtly differently in some of the little things.


  [1]: http://daringfireball.net/projects/markdown/
  [2]: http://www.fileformat.info/info/unicode/char/2163/index.htm
  [3]: http://www.markitdown.net/
  [4]: http://daringfireball.net/projects/markdown/basics
  [5]: http://daringfireball.net/projects/markdown/syntax

```

> The above file is also a great Intro to Markdown. If you didn't know that.

## 4. Creating HTML and Publishing

When the article of yours is written, and safely saved in the content folder. You can burn the heat by firing up the following command in your site's directory.

```
make clean html serve
```

The first word `make` initiates the makefile, accepts the options `clean`, which deletes previous builds. Which are none in your case. Then the `html` is processed to convert to html. The last option `serve` now opens a local server in your computer, which you can access to open your blog. In your favorite browser type `localhost:8000` in address bar and you will have your blog running, but only on your computer.

To publish this on github, copy the contents of output folder to your git repo of branch `gh-pages`. Then push the new commit and open your github site address. ( which normally is something like the following `user_name.github.io/repo_name`)

Viola here is your markdown powered blog ready, now you write articles, and follow the last step to publish.

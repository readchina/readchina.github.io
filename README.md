# Project Webpage
![Jekyll Deploy](https://github.com/duncdrum/forty-jekyll-theme/workflows/Jekyll%20Deploy/badge.svg)

Our new website is currently located at `https://readchina.github.io` and build using [GitHub pages](https://pages.github.com). We use the excellent Jekyll version of the ["Forty" theme](https://github.com/andrewbanchich/forty-jekyll-theme) originally by [HTML5 UP](https://html5up.net/).  

## Requirements
To preview and work on the website on your computer you need to have ruby `2.4.0` or higher  (better to have v3.0.1) and jekyll `4` installed. If you run into issues with your installation please check the full [installation](https://jekyllrb.com/docs/installation/macos/) instructions by jekyll.

If you maintain multiple sites, we recommend using [rbenv](https://github.com/rbenv/rbenv) to manage the parallel installation of mutliple ruby environments. 

For processing word documents and transforming them into pdfs. We use [pandoc](https://pandoc.org/index.html):

```shell
brew install pandoc
```

High Qualiy Pdfs are generated using [LateX](https://www.tug.org/mactex/), you must install this separately before the conversions can take place, its probably best to restart your PC once before doing the first pdf conversion after installing Latex. 

## Installation
You only need to do this once. Use `homebrew` to install the latest ruby.
1.  Either install the latest ruby for your system
    ```zsh
    brew install ruby
    ```
    or use `rbenv`:
    ```shell
    rbenv install 2.7.2
    ```

    (rbenv is recommended for macOS on apple silicon)

1.  Then add ruby to your path (not necessary with `rbnev`)
    ```zsh
    echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
    ```
1.  Now install jekyll
    ```zsh
    gem install --user-install bundler jekyll
    ```

Note: If you are still using `bash` instead of `zsh` type `brew info ruby` to see the correct command for your system.
For `rbenv` users drop the `--user-install` flag when installing gems.

### Upgrading with Homebrew

The current stable version of ruby is 3.0.2.  You can check your ruby version with:

```
ruby -v
```

To upgrade to the latest rbenv and update ruby-build with newly released Ruby versions, upgrade the Homebrew packages:

```
$ brew upgrade rbenv ruby-build
```

### Running locally

Since webrick is no longer a bundled gem in Ruby 3.0, the following command can help you add webrick (You only need to do this once before your run jekyll locally for the first time):

```
bundle add webrick
```

If you have the necessary tools installed. Open this folder in your Terminal (CLI) and type the following.

```zsh
bundle exec jekyll serve
```

You should see something like this:

```zsh
Server address: http://127.0.0.1:4000
Server running... press ctrl-c to stop.
```

Open the [server address](http://127.0.0.1:4000) in your browser and you can see what your changes will look like on the webpage.

You would normally press `ctrl-c` to stop the server in the terminal window. If you can no longer locate that terminal here is a handy shortcut to stop the local server from a new terminal.
```
ps aux |grep jekyll |awk '{print $2}' | xargs kill -9
```

### Content editing
You can follow the links above to a full demo of default features.

There are defaults layouts for `landing`, `page`, `post`, etc.  to be set in your markdown headers, e.g.:

```
layout: allposts
```

Go ahead and edit away ...

### Publishing your changes
To publish you changes commit them into their own branch and open a pull request against the `master` branch. A GitHub workflow will build the site and push to `gh-pages` automatically after your PR has been merged. Do **not** commit changes to `gh-pages` directly.

If you are using the `blog` default, make sure to include the full date of the post in the name of your blog post, e.g.:

```
2020-04-10-exciting-news.md
```

To immediately see your page go live use a date in the past, or otherwise you ll have to wait for the post to become visible.

## Interventions
By popular demand *Interventions* will be drafted using `MS-Word`. We have shared a word-template file on basecamp, download and save it to your computer using the `Save as Template` command in the `File` menu. To start a new Interventions document in Word, us `New from Template`. The citation style should be Chicago (Author-Date) format. Do not use Footnotes!

In order to publish an Intervention we need to 1) convert the word document into mardown, and 2) add the necessary header to the markdown file for the webpage to function. You can use a free tool called [pandoc](https://pandoc.org/index.html) for the conversion. To install it on macOS run.

```shell
brew install pandoc
```

You only need to do this once. 

### File conversion via Pandoc 
Once you have pandoc installed open your terminal app. You have to options either:
- navigate to the folder on your hard-drive where you stored the word document. In this example I have a word document `Pandoc_test.docx` in a folder `Documents/Interventions`. First, navigate into the folder, using `cd` (current directory). Second, tell pandoc to convert the file from (`-f`) word to (`-t`) markdown by creating (`-o`) and new file named `Pandoc_test.md`. 
```shell
cd ~/Documents/Interventions 
 ~/Documents/Interventions/ [1.23.8] pandoc Pandoc_test.docx -f docx -t markdown -o Pandoc_test.md
```

- Alternativey open your terminal, and then drag-n-drop the word document into it using your mouse. 
```shell 
pandoc ~/Desktop/Layout_test.docx -f docx -t markdown -o Layout_test.md
```

### Prepare the markdown file for publishing
Once you have generated a markdown file, you can copy it into the `interventions/` folder in this repo. Remember that the file name will be part of its url, so pick something sensible, and without `whitespaces`, `&`, etc. 

At the very top of the converted markdown file, you need to insert and adjust the header:

```yml
---
layout: post
title: '01: What is a Reading Act?'
author: 'Lena Henningsen'
date: '2021-04-21'
abstract: 'Reading acts emphasize …'
description: 'A READCHINA Intervention'
nav-menu: false
show_tile: false
---
```

You should only adjust `title`, `author`, `date` and `abstract`, use the number format of the example. Don't try to put any links, images etc, into the abstract. Keep it short and simple. 

Once you adjusted the header you can commit your changes and perform a final review of how the intervention will look in a browser. Once you're satsified that contents are correct, italics etc, are where they belong. Open a Pull Request. To brush up on `markdown` see the links below. 

To generate the downloadable `pdf`, use pandoc as well. Open the `interventions/` folder inside your terminal and use the following command, in the example the file name is `What_is`, adjust this to the name of the file you whish to convert making sure that the input and outpu file names **match exactly**:

```shell
pandoc What_is.md --pdf-engine=xelatex --variable CJKmainfont="STSong" -o pdf/What_is.pdf
```

After running this command, a new file should be inside the `interventions/pdf/` folder, which can be downloaded from our webpage once the intervention is published. 

### Further Reading and Tutorials
-   [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
-   [GitHub Pages Documentation](https://help.github.com/en/github/working-with-github-pages)
-   [Programming Historian: Jekyll gh-pages Tutorial](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages)
-   [Google Analytics Dashboard](https://analytics.google.com/analytics/web/provision/#/p272623122/reports/defaulthome)

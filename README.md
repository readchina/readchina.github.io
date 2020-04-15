## Project Webpage
![Jekyll Deploy](https://github.com/duncdrum/forty-jekyll-theme/workflows/Jekyll%20Deploy/badge.svg)

Our new website is currently located at `https://readchina.github.io` and build using [GitHub pages](https://pages.github.com). We use the excellent Jekyll version of the ["Forty" theme](https://github.com/andrewbanchich/forty-jekyll-theme) originally by [HTML5 UP](https://html5up.net/).  

You can follow the links above to a full demo of default features.

There are defaults layouts for `landing`, `page`, `post`, etc.  to be set in your markdown headers, e.g.:

```
layout: allposts
```

### Running locally
After you've cloned this repository, you can preview your changes in your browser before pushing them to GitHub. To view such changes locally on your computer before they are uploaded you need to install [jekyll](https://jekyllrb.com).

If you have the necessary tools installed. Open your Terminal (CLI) and type the following.

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

Go ahead and edit away ...

### Publishing your changes
To publish you changes commit them into their own branch and open a pull request against the `master` branch. A GitHub workflow will then build the site and push to `gh-pages` automatically. Do **not** commit changes to `gh-pages` directly.

If you are using the `blog` default, make sure to include the full date of the post in the name of your blog post, e.g.:

```
2020-04-10-exciting-news.md
```

To immediately see your page go live use a date in the past, or otherwise you ll have to wait for the post to become visible.

### Further Reading and Tutorials
-   [GitHub Pages Documentation](https://help.github.com/en/github/working-with-github-pages)
    -   [Running locally](https://help.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll)
-   [Programming Historian: Jekyll gh-pages Tutorial](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages)
-   [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

**HINT**
The jekyll documentation for macOS still assumes the `bash` shell when adding ruby to your `PATH`. If you are using `zsh` on macOS catalina the command is:
```zsh
echo 'export PATH="$HOME/.gem/ruby/2.7.0/bin:$PATH"' >> ~/.zshrc
```

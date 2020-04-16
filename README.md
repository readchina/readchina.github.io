## Project Webpage
![Jekyll Deploy](https://github.com/duncdrum/forty-jekyll-theme/workflows/Jekyll%20Deploy/badge.svg)

Our new website is currently located at `https://readchina.github.io` and build using [GitHub pages](https://pages.github.com). We use the excellent Jekyll version of the ["Forty" theme](https://github.com/andrewbanchich/forty-jekyll-theme) originally by [HTML5 UP](https://html5up.net/).  

### Requirements
To preview and work on the website on your computer you need to have ruby and jekyll installed. If you run into issues with your installation please check the full [installation](https://jekyllrb.com/docs/installation/macos/) instructions by jekyll.

#### Installation
You only need to do this once. Use `homebrew` to install the latest ruby.
1.  Install the latest ruby
    ```zsh
    brew install ruby
    ```
1.  Then add ruby to your path.
    ```zsh
    echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
    ```
1.  Now install jekyll
    ```zsh
    gem install --user-install bundler jekyll
    ```

(if you are still using `bash` instead of `zsh` type `brew info ruby` to see the correct command for your system.)

#### Running locally
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

#### Publishing your changes
To publish you changes commit them into their own branch and open a pull request against the `master` branch. A GitHub workflow will build the site and push to `gh-pages` automatically after your PR has been merged. Do **not** commit changes to `gh-pages` directly.

If you are using the `blog` default, make sure to include the full date of the post in the name of your blog post, e.g.:

```
2020-04-10-exciting-news.md
```

To immediately see your page go live use a date in the past, or otherwise you ll have to wait for the post to become visible.

### Further Reading and Tutorials
-   [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
-   [GitHub Pages Documentation](https://help.github.com/en/github/working-with-github-pages)
-   [Programming Historian: Jekyll gh-pages Tutorial](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages)

## Team 8: Code Cards

Code Cards 🃏 is a revolutionary studying tool, letting anyone learn anything. 

Features:
- Variety of studying methods such as flashcards and quizzes so that users are thoroughly tested
- Revolutionary statistics tracker 📊, allowing users to review what mistakes they have made so they can focus on their weakest areas
- Huge database of flashcards 
  - Can be updated by huge userbase or by direcly uploading a link to Quizlet flashcards
  - Can be kept public or private
- Interactive search bar 🔎, letting users find exactly what they need at ease
- Secure signup and login system 🔑 using Json Web Tokens, preventing any malicious attackers from stealing user information

Previews:

![Login](assets/img/previews/Screenshot%202023-02-26%20at%207.28.11%20PM.png)

Secure Login System

![Search](assets/img/previews/Screenshot%202023-02-26%20at%207.29.12%20PM.png)

Huge Flashcard Database

![Flashcards 1](assets/img/previews/Screenshot%202023-02-26%20at%207.30.42%20PM.png)

![Flashcards 2](assets/img/previews/Screenshot%202023-02-26%20at%207.30.05%20PM.png)

Flashcards

![Quizzes](assets/img/previews/Screenshot%202023-02-26%20at%207.32.57%20PM.png)

Practice Quizzes

![Importing](assets/img/previews/Screenshot%202023-02-26%20at%207.31.45%20PM.png)

Importing from Quizlet



Start studying with Code Cards 🃏 today!

https://csa.rohanj.dev/


If your ubuntu version is old, upgrading ruby
```bash
wget http://ftp.ruby-lang.org/pub/ruby/2.7/ruby-2.7.1.tar.gz
tar -xzvf ruby-2.7.1.tar.gz
cd ruby-2.7.1/
./configure
make
sudo make install
```

Installation
```bash
apt install ruby-bundler
bundle install
```
Also update ruby initially to make sure there is compatibility, then install the bundler to be able to use the gemfile and install packages.

Usage

1. Midnight Theme. Use the GitHub Pages [Midnight Theme](https://github.com/pages-themes/midnight/blob/master/README.md) as a resource.  This project started with customization of _layouts/default.html from the Midnight Theme.  If you wanted to use a different [GitHub Pages Themes](https://pages.github.com/themes/), you would similarly change `_layouts/default.html` from repo used to support that theme.  Observe comment at top of _layouts/default.html ...

```html
<!-- 
  _layouts/default.html
  customization to original Midnight theme 
  found through GitHub Pages Themes
 -->
```

2. Preview Site (Option A) - [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).  This instruction provides instructions for ruby `Gemfile`,`bundle install`.  As an addition add `.gitignore` to avoid seeing build files in commit.   After pre-requisites run this command to obtain prompt for web server ...

```bash
bundle exec jekyll serve -H 0.0.0.0 -P 4001 # -H and -P are optional
```

3. Preview Site (Option B) - [GitHub Pages Ruby Gem](https://github.com/github/pages-gem) has additional information on making a local server.  Ruby requirements are the same: `Gemfile`,`bundle install`.   This README looks like basis of FastPages `make server` as it uses Docker and shows how to setup a `Makefile`.

4. Customizing style (CSS).  This project uses `/assets/css/style.scss` as the location to customize your CSS. To avoid warnings in VSCode make sure you install `SCSS IntelliSense` plugin.  To understand default style, make sure you ***Preview Site*** and refer to build generated `_site/assets/css/style.css` (this is worth 1000 lectures).  For the reunion site `gallery.md` uses custom style from `assets/css/style.css` to support 3 images per row.  Observe file and position of import and custom CSS, order is important as clarified in Midnight Theme readme. ...

```css
---
---

@import "{{ site.theme }}";

/* "row style" is flexible size and aligns pictures in center */
.row {
    align-items: center;
    display: flex;
  }
  
  /* "column style" is one-third of the width with padding */
  .column {
    flex: 33.33%;
    padding: 5px;
  }
```


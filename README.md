# UMS Hyperloop Website

This is the repository of UMS Hyperloop official website.

<hr>

**Table of Content**

- [Software Team](#software-team)
- [Installation](#installation)
  - [Requirements](#requirements)
  - [Clone Repository](#clone-repository)
  - [Install Jekyll](#install-jekyll)
- [Development](#development)
  - [Test Jekyll](#test-jekyll)
  - [Make a New Page](#make-a-new-page)
  - [Make a New Post](#make-a-new-post)
  - [Edit HTML Layout](#edit-html-layout)
  - [Edit CSS Style](#edit-css-style)


<hr>

## Software Team

**Lead**: Monica Noori Saghar

- Celik Berk Altingok
- Diane Tobit
- Fauzi Pradipta
- Haruna Yamakawa
- Nadya Djojosantoso

## Installation

### Requirements
* [GitHub App](https://desktop.github.com/)
* [Ruby](https://www.ruby-lang.org/en/downloads/)

### Clone Repository

**Using GitHub App:**
1. Open the GitHub app.
2. Click File > Clone Repository.
3. Search and click 'ums-dvc/ums-dvc.github.io'.
4. Click clone.
5. To open the folder, click Repository > Show in Explorer.

**Using Command Line:**
1. Copy `https://github.com/ums-dvc/ums-dvc.github.io.git`.
2. Open command line or terminal.
3. Type `git clone` (with space at the end) and then paste the repository URL.
4. Navigate to the folder using `cd ums-dvc.github.io`.

### Install Jekyll

In the command line or terminal, type `gem install jekyll bundler`.

## Development

### Test Jekyll

To run the server and see the changes that you've made:

1. Open command line or terminal at the project folder.
2. Type `bundle exec jekyll serve`.
3. In your browser, go to `localhost:4000`.

Note: The server automatically updates the local website if you change something while the server is on.

To stop the server, press Ctrl + C and then type `y`, or just close the command line.

### Make a New Page

1. In the project folder, create a new Markdown or HTML file (e.g. `your-page.md` or `your-page.html`).
2. At the top of the file, write:

  ```
  ---
  layout: page
  title: your-page-title
  permalink: /your-page-link/
  ---
  ```

  Note: The layout has to be `page` or the name of a custom layout (see [Edit HTML Layout](#edit-html-layout)).

3. Add the page content after the last line. If you're using Markdown, see [Markdown guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Make a New Post

1. Navigate to the `_posts` folder.
2. Create a new file with the name format `YYYY-MM-DD-your-page-title.md`.
3. At the top of the file, write:

  ```
  ---
  layout: post
  title:  "Your Page Title"
  date:   YYYY-MM-DD hh:mm:ss -0800
  categories: update
  ---
  ```

  Note: The layout has to be `post`.
  
4. Add the post content after the last line. If you're using Markdown, see [Markdown guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).


### Edit HTML Layout

To create your own page layout:
1. Navigate to the `_layouts` folder.
2. Create a new HTML file (e.g. `mypage.html`).
3. At the top of the file, write:

  ```
  ---
  layout: default
  ---
  ```

4. Add the HTML layout after the last line.
5. Use this to place your page content:

  ```html
  <div class="post-content">
    {{ content }}
  </div>
  ```

### Edit CSS Style

Edit the file at `\assets\main.scss`.

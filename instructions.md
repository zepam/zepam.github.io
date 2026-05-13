Use Jekyll locally for previewing without deploying.

In terminal, go to the repo directory:
`cd zepam.github.io`

~~Install dependencies once: bundle install~~

Run local server:
`bundle exec jekyll serve --livereload`

Open:
http://127.0.0.1:4000


------

This site is a <a href="https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll">Jekyll</a> <a href="https://pages.github.com/">GitHub Pages</a> site. 
Content is in Markdown files. Style is in style.scss. 

Jekyll reads front matter and Liquid templates then GitHub Pages serves the generated static HTML. The shared template is `_layouts/default.html` and the styling comes from `style.scss`, which imports the selected Jekyll theme and then overrides the look and feel.

Homepage: `index.markdown.` This file loops over Jekyll collections as defined in `_config.yml`: projects, talks, papers, posters, and fun. Each item file in folders stores data such as title, date, thumbnail, description, and external links. The homepage uses that metadata to render the files into formatted text.

Page-by-page, the site works like this:

`/` comes from `index.markdown` and shows Education, Current Projects, Talks, Papers, Posters, Fun, and Past Projects.

`/projects/...` pages are generated from the files in `_projects/`, with each markdown file becoming its own project page.

`/papers/...`, `/talks/...`, `/posters/...`, and `/fun/...` are generated from the corresponding collection folders, with custom permalink rules set in `_config.yml`.

The top bar and footer are shared includes from `header.html` and `footer.html`.

A small bit of JavaScript in default.html makes images inside project content clickable, but the site is otherwise primarily static HTML generated at build time.
# Big picture of Jekyll

This is a template for starting your own mock journal! In the `journal-site` branch you can see my deployed site; this branch is the template.


## Jekyll

The following template is a Jekyll implementation of a journal website. Jekyll is a static site generator, which means it is a software that generates HTML and CSS files from markdown files or templates that you specify. For more information on how to get started with Jekyll, see the [documentation](https://jekyllrb.com/), especially [this tutorial series](https://jekyllrb.com/tutorials/video-walkthroughs/). This template is based around the "minimal mistakes" Jekyll theme: [theme documentation](https://mmistakes.github.io/minimal-mistakes/). 

What Jekyll takes as input is a markdown document with **variables**: at the top of a document (between --- lines) are a bunch of variable definitions, e.g.
```
---
title: thing
othervar: stuff
---
```
Jekyll then uses those variables (in this case `title` and `othervar`) in a template that uses the values of the variables to render an html document (a webpage). The theme (or this template) does some pretty fancy processing to end up with the site you see rendered. 

## What Jekyll can't do
Jekyll can't programatically generate the markdown files. Which is a shame, because database-driven sites (that have many pages, e.g. articles, that are similar with different titles, abstracts, etc.). Ideally, we would want to have some sort of database that stores information about all the manuscripts, maybe some data about each issue of the journal and generates the markdown files that then generate the website. Since Jekyll can't do this, I made a MATLAB script that can. You can find that in the `Utilities` directory. 

# How to use this template

## Configure the site
In the `config.yml` file you will find declarations of all site variables. Change things like the title, URL, etc. Most importantly, under `collections: ` you will need an entry for each issue (e.g. `vol1-1`) and set its `output: true`. This will look for pages in the corresponding directory (the collection name with a leading underscore, e.g. `_vol1-1`) to render the markdown files there into webpages.

## Add your database
The manuscript database is found at `Utilities\Manuscript.csv`. Each row will generate a page in the right collection directory. One row there that is structurally important for the website is `Section`. These are the topics in the issue. the `Issue.csv` database holds some more detailed metadata on these. The matlab script generates the following:
- **Article pages:** these are found in the collection directory. Uses the `template` file to generate these.
- **Section pages:** these are found in the `_pages` directory. Uses the `template_collection.html` file to generate these.
- **authors.yml:** a database of the unique authors from the manuscript database, goes in the `_data` directory.
- **sections.yml:** a database of the issue section metadata, also goes in the `_data` directory.
- **navigation.yml:** the database that controls the navigation bar at the top of the screen. Also in the `_data` directory

## Script templates
The two templates (article and section above) can be edited. The main thing you will probably want to do is change the color or background image of the banner at the top of the page. These are found as 
```
header:
  overlay_image: banner.svg
  overlay_filter: rgba(r,g,b,alpha)
```
Change these to customize the header of your page. You will also need to change these manually on every other site page (see below for list).

## Customizing the color settings
You can customize the color settings by changing some CSS variables in `_sass/minimal-mistakes/_variables.scss`. Especially I would recommend changing `$primary-color` and `$header-color` as these are some of the most frequently used colors on the site.

## Manually changing the main pages
Here is a list of all the pages you will need to go in and manually change. 

### Only change front matter variables
- **`/index.md`**: The home page of the website. Much of this will need to be changed, only the collections list is automatic, all the other content (cf. `feature_row` variables) is manually generated.
- **`/_pages/highlights.md`**: the editor's suggestions archive.
- **`/_pages/vol1-1.md`**: the entire issue archive. You will need to copy this to add other issues (not supported yet).
- **`/Utilities/template`**: the template for generating the article files. Note that `{{!Varname}}` substitutes variables according to the header names in `Manuscript.csv`.
- **`/Utilities/template_collection.csv`**: the template for generating the section archive pages. Note that `{{!Varname}}` substitutes variables according to the header names in `Issue.csv`. 


### Also change the content of the file
- **`/_pages/about.markdown`**: Customize the about page for your journal
- **`/_pages/authors.md`**: The author information page for your journal
- **`/_pages/submissions.md`**: The author information page for your journal

# Happy journaling!

This should be all you need to get started on your own mock journal website! Best of luck using this resource.









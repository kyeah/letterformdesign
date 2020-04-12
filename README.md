type-site
=========

## Directory Structure

```
└── _layouts       # page layouts
└── _includes      # page components
└── _projects      # project definitions in markdown
└── assets         # public assets (css, js, imgs)
└── index.md       # homepage
└── about.md       # about page
└── project.md     # page for an individual project
```

## Working structure

```
*.md
=> uses a layout in _layouts
   => uses components in _includes
```

Reusuable page components, such as the header, are defined in `_includes`. These page components are used as part of page layouts in `_layouts`.

When someone visits a page, the URL identifies which `*.md` file to use, such as index.md (for the homepage) or `about.md` for the about page. The markdown file refers to a layout, which tells us how to render the page.

`project.md` is a special layout that generates multiple pages based on the `_projects` collection. For each markdown file in `_projects`, a page is generated with this template and the associated metadata from the `_projects/*.md` file. In this way, the homepage can iterate over all `site.projects` and link to the generated `project.url` for each project.

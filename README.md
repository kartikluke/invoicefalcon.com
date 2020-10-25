# invoicefalcon.com
Website for InvoiceFalcon built using [Jekyll](https://jekyllrb.com/docs)

## Setting up
- Install Jekyll globally with `gem install bundler jekyll` (Documentation https://jekyllrb.com/docs/installation/)
- Install dependencies with `bundle install`
- Run website locally with `jekyll serve`. It should be available at http://127.0.0.1:4000/

## Deployment
- Once changes are made, you can build the site for production use using `jekyll build`.
- Commit the changed files into git and push it to Github where it will automatically be uploaded to the Github page.

## Content

Content for this website is generated as Markdown files (supports direct HTML as well) with some tags at the top known as [frontmatter](https://jekyllrb.com/docs/front-matter/). The Markdown also supports [liquid templating](https://jekyllrb.com/docs/liquid/) that can use custom [variables](https://jekyllrb.com/docs/variables/) to fill in content.

### [Pages](https://jekyllrb.com/docs/pages/)

```
---
title: Help Center
url: '/help'
---
```

Adding a new file in this format file.md in the root directory with the above frontmatter will create available page on the website.

### [Posts](https://jekyllrb.com/docs/posts/)

```
---
layout: post
title:  "How does the Pay-as-you-go plan work?"
category: [Pricing]
teaser: "Read more about our Pay-as-you-go pricing plan, designed to help you focus on running your business."
---
```

Adding a new file in this format 2012-09-12-how-to-write-a-blog.md with the above frontmatter will add a new post to the website. Currently all posts show up in the help.md page. They get split into the different categories by the category variable and the teaser is the text we see in the help section card.

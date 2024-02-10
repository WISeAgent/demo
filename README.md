---
title: Sample Markdown Site with Embedded HTML
author: Your Name
description: A sample site that demonstrates how to embed HTML code in markdown files
---

# Sample Markdown Site with Embedded HTML

## 1. Embed raw HTML content with a div that has the content "helloworld"

This is an example of how to embed raw HTML content in a markdown file. You can use any HTML tags directly in the markdown file, but make sure they are not indented or wrapped in paragraphs. The HTML code will be rendered as it is in the browser. For example:
```MD
{% raw %}
    <div>helloworld</div>
{% endraw %}
```
<div>helloworld</div>

## 2. Embed raw HTML with a script tag that prints alert(1)

This is an example of how to embed raw HTML with a script tag that prints alert(1) in a markdown file. Script tags can execute JavaScript code in the browser, which may show an alert box with the number 1 when the markdown file is rendered as HTML. However, be careful when using script tags in markdown, as they may pose security risks or cause unexpected behavior.

{% raw %}
    <script>alert("greetings");</script>
{% endraw %}
<script>alert("greetings");</script>

## 3. Embed HTML content from an external page, such as sample.com

This is an example of how to embed HTML content from an external page in a markdown file. You can use a static site generator like DocFX to include the HTML content from another file or URL in your markdown file. You need to use a special marker to indicate the start and end of the HTML inclusion. For example:

**Sample for DocFX**  It'll render as plain-text as-it-is in github static hosting as it uses Jekyll generator.
``` #MD
< !-- BEGIN INCLUDE http://example.com/ -->
< !-- END INCLUDE -->
```

**Sample for Jekyll** If the included file doesn't exist, it'll failed the the deploy task in github action
```MD
{% raw %}
    {% include_relative sample.com %}
{% endraw %}
```

> sample error reported in https://github.com/WISeAgent/demo/actions/runs/7850893429  
> build
 Logging at level: debug GitHub Pages: github-pages v229 GitHub Pages: jekyll v3.9.4 Theme: jekyll-theme-primer Theme source: /usr/local/bundle/gems/jekyll-theme-primer-0.6.0 Requiring: jekyll-github-metadata Requiring: jekyll-seo-tag Requiring: jekyll-coffeescript Requiring: jekyll-commonmark-ghpages Requiring: jekyll-gist Requiring: jekyll-github-metadata Requiring: jekyll-paginate Requiring: jekyll-relative-links Requiring: jekyll-optional-front-matter Requiring: jekyll-readme-index Requiring: jekyll-default-layout Requiring: jekyll-titles-from-headings GitHub Metadata: Initializing... Source: /github/workspace/. Destination: /github/workspace/./_site Incremental build: disabled. Enable with --incremental Generating... Generating: JekyllOptionalFrontMatter::Generator finished in 9.037e-06 seconds. Generating: JekyllReadmeIndex::Generator finished in 4.619e-06 seconds. Generating: Jekyll::Paginate::Pagination finished in 2.435e-06 seconds. Generating: JekyllRelativeLinks::Generator finished in 0.000649503 seconds. Generating: JekyllDefaultLayout::Generator finished in 0.001453351 seconds. Generating: JekyllTitlesFromHeadings::Generator finished in 1.1341e-05 seconds. Rendering: README.md Pre-Render Hooks: README.md Rendering Liquid: README.md github-pages 229  
| Error: Could not locate the included file 'sample.com' in any of ["/github/workspace/"]. Ensure it exists in one of those directories and is not a symlink as those are not allowed in safe mode. 

**iframe** 
This will create a frame that displays the content from external page within your static page.
However, please note that some websites may not allow embedding their content in an iframe, due to security or privacy reasons. They may use the X-Frame-Options HTTP header to prevent cross-origin framing. In that case, you will see an error message instead of the content. youtube.com is an example.

```MD
{% raw %}
   <iframe src="https://wwang.atlassian.net/wiki/spaces/~13820020/pages/669057097/Dynamic-Link+Libraries#Introduction" width="300" height="300"></iframe>
{% endraw %}
```
<iframe src="https://wwang.atlassian.net/wiki/spaces/~13820020/pages/669057097/Dynamic-Link+Libraries#Introduction" width="300" height="300"></iframe>




---
title: Sample Markdown Site with Embedded HTML
author: Your Name
description: A sample site that demonstrates how to embed HTML code in markdown files
---

# Sample Markdown Site with Embedded HTML

## 1. Embed raw HTML content with a div that has the content "helloworld"

This is an example of how to embed raw HTML content in a markdown file. You can use any HTML tags directly in the markdown file, but make sure they are not indented or wrapped in paragraphs. The HTML code will be rendered as it is in the browser. For example:

<div>
helloworld
</div>

## 2. Embed HTML content from an external page, such as sample.com

This is an example of how to embed HTML content from an external page in a markdown file. You can use a static site generator like DocFX to include the HTML content from another file or URL in your markdown file. You need to use a special marker to indicate the start and end of the HTML inclusion. For example:

{% include_relative sample.com %}

<iframe src="https://sample.com" width="300" height="300"></iframe>


## 3. Embed raw HTML with a script tag that prints alert(1)

This is an example of how to embed raw HTML with a script tag that prints alert(1) in a markdown file. Script tags can execute JavaScript code in the browser, which may show an alert box with the number 1 when the markdown file is rendered as HTML. However, be careful when using script tags in markdown, as they may pose security risks or cause unexpected behavior.

<script>
alert(1);
</script>

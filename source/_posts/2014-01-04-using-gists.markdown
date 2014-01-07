---
layout: post
title: "Including Gists and other code"
date: 2014-01-04 15:58:59 +0200
comments: true
categories:
---

Embedding code, by pasting, including files, including gists in the octopress blog.  Here are some notes about styles and ways of quoting code, and a test.
<!--more-->

### Ways to include code ###

#### Backticks ` ####


http://octopress.org/docs/plugins/backtick-codeblock/

    ``` [language] [title] [url] [link text] [linenos:false] [start:#] [mark:#,#-#]
        code snippet
    ```
#### Include Code ####

http://octopress.org/docs/plugins/include-code/

    {% raw %}
    {% include_code [title] [lang:language] path/to/file [start:#] [end:#]
       [range:#-#] [mark:#,#-#] [linenos:false] %}
    {% endraw %}

### Better styles for gist includes ###

From: https://gist.github.com/jnrbsn/578379

    /* Better styles for embedding GitHub Gists */
    /* From: https://gist.github.com/jnrbsn/578379 */
    .gist{font-size:13px;line-height:18px;margin-bottom:20px;width:100%}
    .gist pre{font-family:Menlo,Monaco,'Bitstream Vera Sans Mono','Courier New',monospace !important}
    .gist-meta{font-family:Helvetica,Arial,sans-serif;font-size:13px !important}
    .gist-meta a{color:#26a !important;text-decoration:none}
    .gist-meta a:hover{color:#0e4071 !important}

### Test ###

{% gist 8071915 lhcsc %}

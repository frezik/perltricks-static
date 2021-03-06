PerlTricks.com
==============

[PerlTricks.com](http://perltricks.com) is a website dedicated to Perl programming code and community news.

If you're interested in writing for PerlTricks.com read the guide below; you can send us a pull request with your article or just email the editor (`editor@perltricks.com`) if you have any questions. We're always looking for new writers and material!

Technology
----------
The website is built with [Hugo](http://gohugo.io) and hosted on GitHub Pages.

Style Guide
===========
This section is intended to guide PerlTricks authors in producing articles that are consistent with the aims of the website. None of this is set in stone - great writing should always prevail.

Goal
----
We aspire to reasoned, insightful, professional writing with a lighthearted bent.

Topics of interest
------------------
- Anything Perl related: news, events, tutorials, community
- Non-Perl programming subjects: version control, hosting, sysadmin, search
- Open Source tools and techniques

Looking for an idea for an article? Our bread and butter is: "here is something cool you can do with Perl". Start there.

Politics / Tone
---------------
- We are pro: Perl, Open Source and free software
- No rants or "hit pieces"
- Reasoned criticism is fine

Language
--------
- American English
- 300-1,000 words per article
- Simple English (use http://www.hemingwayapp.com/ to help)
- Only capitalize the first letter of a word in headings (no title case)
- Articles can begin with an italicised introductory paragraph
- Prefer the first-person
- We are "PerlTricks.com"
- You can use "we" to refer to PerlTricks.com, the staff, our point of view etc.
- When referring to Perl modules for the first time, provide a link to metacpan

Markup
------
Articles are written in [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). Every article is prefaced with [front matter](http://gohugo.io/content/front-matter/) in JSON.

The front matter contains the article metadata. Here's an example for a recent article:

``` json
  {
     "tags" : [
       "tie",
       "scalar",
       "callback",
       "cycle"
     ],
     "title" : "Magical tied scalars",
     "description" : "Subvert and simplify code with tied scalars",
     "authors" : [
        "brian d foy"
     ],
     "date" : "2016-02-16T09:50:00",
     "draft" : true
  }
```

Older articles also have the `slug` attribute, which determines the URL of the article. This isn't necessary anymore (it's used to preserve historic URLs for articles from our old site). Instead just name the file the same as the title of the article, but in lowercase and with spaces replaced with hypens (`-`). In this example case, the filename is `content/article/magical-tied-scalars.md`. 

Once `draft` is changed to `false`, the article will be listed on the website at `perltricks.com/article/magical-tied-scalars`. So when providing a pull request, keep this as `true`. The site editor will switch this to `false` once the article is ready to be published.

Titles-as-filenames has another benefit: no two articles can have the same title, which avoids issues with 2 articles having duplicate URLs.

The front matter is provided inline in the markdown file, immediately followed by the article body, in GitHub flavored markdown. The two main rules to know here are as follows:

If you want highlighted code syntax, use a fenced code block with the `prettyprint`  keyword:

    ``` prettyprint
      code
      code
      code
    ```

Code is highlighted using `prettify.js` and it will automatically detect the code type and provide the appropriate syntax highlighting (it's not perfect, but good enough).

Otherwise just use a code block (fenced or indented style) and it will be displayed in monospace on a dark background. This is used for showing data and terminal commands.

The other thing to know is article subheadings are size `h3`. So use the following construct

    ### Subtitle goes here

The article metadata like author, title and date are contained in the front matter and not needed in the article markdown body.

See the `content/article` directory for more complete examples of our articles.

&copy; PerlTricks.com


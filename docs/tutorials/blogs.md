# Blog Tutorial

## 1. Overview
__Content:__ The tutorial will guide you through the process of configuring the
[blog plugin], creating posts, setting up authors, producing an RSS feed as well
as... <!-- TODO -->

[blog plugin]: ../../plugins/blog

__Prerequisites:__ This tutorial assumes that you have installed either the
[public version] or the [Insiders edition] of Material for MkDocs and that you have
worked through the [Creating your site] setup guide. Note that where features of
the Insiders edition are used, these will be marked with the heart icon:
<!-- md:sponsors --> If you are using the public version then you can skip these
steps.

[public version]: ../../getting-started
[Insiders edition]: ../../insiders/getting-started
[Creating your site]: ../../creating-your-site


__Outcomes:__ After working through the tutorial, you will have learned how to
produce a professional or personal blog to engage with your audience. You will
know and have experienced how the blog plugin ab be used in combination with
other features and third-party plugins to achieve this.

__Time required:__ To run through this tutorial in full you will typically need
to have about XX minutes of time. Note that the time it takes will depend on a
number of factors, so this is only a rough estimation based on our experience
and testing.

## 2. Introduction

Blogs are a great way to engage with your audience. Software developers can use
a blog to announce new features, demonstrate their usage and provide background
information. You can demonstrate competence by commenting on the state of the
art or document your own work as best practice. Posts on current topics can help
draw in visitors for your main website and can keep your audience engaged. Of
course, you can blog about any topics close to your heart.

The [blog plugin] makes running a blog alongside your other content easy but you
can also configure it to run a stand-alone blog if posts are the only kind
of content you need. It becomes even more powerful when used in combination with
other features of Material for MkDocs such as the [tags plugin] or with third
party plugins such as the [RSS plugin].

[tags plugin]: ../../plugins/tags
[RSS plugin]: https://guts.github.io/mkdocs-rss-plugin/

!!! example "Explore the Material for MkDocs Blog"

    Take a moment to look at the [Material for MkDocs blog] to see what elements
    a blog consists of before moving on to the next section. What makes the blog
    different from the rest of the site?

[Material for MkDocs blog]: https://squidfunk.github.io/mkdocs-material/blog/

## 3. Key concepts

A blog consists of a number of self-contained _posts_ (also often called
articles).

An index page shows the posts in reverse chronological order, with the most
recent post at the top. It usually shows only a short _excerpt_ and a link that
the user can click to navigate to the full post.

Both the index page and the post itself will usually list information such as
when the post was published, when it was updated, who the author is and what the
expected reading time is.

Since the blog posts are primarily arranged by time and not into a hierarchy,
their URLs do not reflect such a structure. Instead, each post's URL usually
contains a shortened description, the _slug_.

The main navigation structure is the timeline, which can be subdivided into
_categories_. In addition, posts can be _tagged_ to provide an additional
navigation structure based on content rather than time of posting.

The navigation elements in the blog are the timeline, with the main index page
showing a given number of posts and an _archive_ section allowing access to
older posts, organised be year. The _categories_ section provides access to
index pages for the category index pages. In addition, when tagging is used, tag
index pages may also be available in the navigation.

An _author index_ may show all the posts by an individual author. Each author
may also have a profile page that provides more information about them. The two
can be integrated.

Finally, an _RSS feed_ allows users to subscribe to a blog so that they get
notified when new posts are published. RSS Feed readers are often used to access
blogs that a user follows. They usually support downloading the blog content for
offline consumption.

## 4. Setting up a blog

The blog plugin is part of Material for MkDocs but needs to be configured in the
`mkdocs.yml`.

!!! example "Set up a blog"

    If you have not done so already, create a project for your blog:

    === "MacOS/Linux"
        ```bash
        $ mkdocs new myblog
        $ cd myblog
        ```

    === "Windows"
        TODO

    Then edit the `mkdocs.yml` file in the newly created directory to make sure
    if has the following content:

    ```yaml
    site_name: Blog Template

    theme:
      name: material

    plugins:
      - search
      - blog
    ```

The blog plugin will create a directory structure for your blog posts if it does
not exist, so simply run a MkDocs build:

!!! example "Create directory structure"

    === "MacOS/Linux"
        ```bash
        $ mkdocs build
        $ ls -R docs
        blog		index.md

        docs/blog:
        index.md	posts

        docs/blog/posts:
        ```
    === "Windows"
        TODO

Now you can create your first blog post in `docs/blog/posts`. You can use any
naming convention and directory structure you like for your posts, as long as
they are inside  `docs/blog/posts`.

Each post _must_ have a page header, which appears at the top of the Markdown
code between lines with three dashes. Within this header, you need to have at
least a `date` entry but you can add other data, as you will see below.
Following the header comes the page content, which is any Markdown. Note,
however, that it is important to have a level one heading as this will be used
to produce the _slug_. Also, you can define where the extract will end that is
shown on the index page by adding `<!-- more -->` (an HTML comment) to the page.

!!! example "Write your first post"

    Create a file `docs/blog/posts/myfirst.md` with the following contents:

    ```
    ---
    date: 2023-12-31
    ---

    # Happy new years eve!

    We hope you are all having fun and wish you all the best for the new year!
    <!-- more -->

    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua.
    ```

    Then, run `mkdocs serve` and point your web browser at
    `http://localhost:8000/blog`.

    Observe how the blog plugin automatically creates navigation elements for
    the blog. Later on we will see how this can be integrated into navigation
    for a site that contains not just a blog. Note the other elements of a blog
    are present and only an extract is shown. When you select the "Continue
    reading" link, you will get to the full blog post. Note how it has a URL
    generated from the first-level heading.

## 5. Drafts, edits, pinning, slugs

You may want to produce a draft of a blog post and work with it locally but
exclude it from the build that you will publish until it is finished. You can
add a field to the page header to indicate that a post is still in draft form
and should not be published.

!!! example "Create a draft"

    Create a second blog post in `docs/blogs/posts/draft.md` with the following
    contents:

    ```
    ---
    date: 2024-01-01
    draft: true
    ---

    # Happy new year!

    Happy 2024 to everyone. Wishing you all the best!
    <!-- more -->

    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua.
    ```

    Now, note how the draft appears on the index page but with a label that
    indicates that it is a draft. Now, crucially, when you run `mkdocs build`,
    the draft will not appear in the output:

    === "MacOS/Linux"
        ```
        $ mkdocs build
        $ ls site/blog
        2023		archive		index.html
        ```

    === "Windows"
        TODO

    The first blog post for 2024 is not there yet because it is still in draft
    stage. Remember to remove the `draft` setting in the header when it is time
    to publish it.

If you are using the [Insiders edition], you can also create
a folder to keep your drafts in and use the [Meta plugin] to add the
`draft` header setting to all the posts in that folder.

[Meta plugin]: ../plugins/meta.md

!!! example "Drafts using the Meta plugin<!-- md:sponsors -->"

    You first need to activate the plugin in your `mkdocs.yaml`:

    ```yaml hl_lines="4"
    plugins:
      - search
      - blog
      - meta
    ```

    Now create the folder for 

    === "MacOS/Linux"

        ```bash
        $ mkdir docs/blog/posts/drafts
        ```

    === "Windows"
        TODO

    Now, within this folder, crate a file `.meta.yml` that contains:

    ```yaml
    draft: true
    ```

    Add another blog post and store it in `docs/blog/posts/drafts`. When you
    look at it locally, you will see the label that identifies it as a draft,
    while in the version built for publication it does not appear. To move a 
    post from draft status to published, simply move it outside `drafts/`.

Sometimes, bloggers need to update a post. This might happen when they have made
a mistake or when something changes that need to be reflected in the post. It is
good practice to indicate that a post has been edited. One way this can be done
is to include an edit date in the page header:

!!! example "Editing a post"

    Make a change to your first blog post, then add an edit date to the header:

    ```hl_lines="3"
    ---
    date: 2023-12-31
    updated: 2024-01-02
    ---
    ```

Sometimes, blog authors want to 'pin' a specific post so that it will always
appear at the top of the index page, no matter what else gets published. If you
are using the [Insiders edition], you can achieve this by adding the `pin` 
attribute in the page header:

!!! example "Pin a post <!-- md:sponsors -->"

    Add the `pin` attribute to your first blog post:

    ```hl_lines="4"
    ---
    date: 2023-12-31
    updated: 2024-01-02
    pin: true
    ---
    ``` 
    
    Observe how this makes the post appear on top of the index page even though
    its publication date is prior to other posts.

Another useful header attribute is `slug`, which allows you to define the slug
for your post instead of having it auto-generated by the Blog plugin. 

!!! example "Change slug"

    If, for example, you wanted the slug to be 'ny-eve'  instead of the somewhat
    lengthy 'happy-new-years-eve', you could add the following:

    ```hl_lines="5"
    ---
    date: 2023-12-31
    updated: 2024-01-02
    pin: true
    slug: ny-eve
    ---
    ``` 
    
    The URL for this post should now be
    `http://localhost:8000/blog/2023/01/31/ny-eve/`.
    

## 6. Defining authors

If your blog has more than one author then you may want to identify the author
for each blog post. The blog plugin allows you to create a file that contains
the author information and to then reference the authors of a particular post in
the page header.

!!! example "Create author info"

    Create a file `docs/blog/.authors.yml` with this content:

    ```yaml 
    authors:
      material:
        name: Material Team
        description: Creator
        avatar: https://simpleicons.org/icons/materialformkdocs.svg
      mkdocs:
        name: 
    ```

    and then add a line to the header of the first post:


    ```hl_lines="4-5"
    ---
    date: 2023-12-31
    updated: 2024-01-02
    authors:
      - material
    ---
    ```

    Note that `authors` is a list, so you can specify multiple authors. is a
    list, so you can specify multiple authors, as you will see below.

With the Insiders edition, you can create custom author index pages that
can highlight the contributions of an author as well as provide additional
information about the author.

!!! example "Add author page <!-- md:sponsors -->"

    First, you need to enable author profiles in the `mkdocs.yml`:

    ```yaml
    plugins:
      - search
      - blog:
          authors_profiles: true
    ```

    Check your blog to see that there is now an extra entry in the main
    navigation next to `archive` and `categories` that lists the authors and
    their contributions.

    To customize the author page, you can create a page that overrides the one
    generated by default. First, create the `author` directory that the profile
    pages will live in:

    === "MacOS/Linux"
        ```
        $ mkdir docs/blog/author
        ```

    === "Windows"
        TODO

    Then create a page `docs/blog/author/material.md`:

    ```
    # The Material Team

    A small group of people dedicated to making writing documentation easy, if
    not outright fun! Here are some of the things we have blogged about:
    ```

    As you can see, the author index gets appended to the content you have
    written in the Markdown file.

## 7. Integrating Navigation

So far, you have let the Blog plugin and MkDocs worry about navigation. For some
use cases, this might be enough and it is simple sufficient to not declare a
`nav` section in the `mkdocs.yml`. 

However, in many projects a blog needs to be integrated with other content and a
navigation structure that is defined in the `nav` section of the configuration.
In such cases, you need to provide a place where the Blog plugin is meant to
attach the blog navigation to the rest of the navigation structure.

Note that all you need to do is to add an entry 

!!! example "Integrate with site navigation"

    Add the following to your `mkdocs.yml` to see how the Blog plugin can
    integrate the blog navigation with the overall navigation structure.

    ```yaml hl_lines="5"
    nav: 
      - Home: index.md
      - Install: install.md
      - Usage: usage.md
      - Blog:
         - blog/index.md
    ```

    You will notice that "Blog" is duplicated in the navigation structure. To
    avoid this, you can use the `navigation.indexes` feature:

    ```yaml hl_lines="3 4"
    theme:
      name: material
      features:
        - navigation.indexes
    ```

## 8. Using categories

Categories are a way to make blog posts accessible by topic while retaining
the navigation structure based on chronology within each category listing.
Use categories when there is a limited set of non-overlapping categories that
your posts can be organised into.

Categories appear in the main navigation, so are directly accessible from there.
This implies that there are relatively few categories as otherwise the
`categories` section in your main navigation will become too crowded.


!!! tip "Single or multiple categories?"

    While it is traditionally the case that a blog post would belong to only
    one category, Material for MkDocs actually allows you to assign multiple
    categories. While this gives you a degree of freedom, you should
    probably not use this too much, not least because you can use tags to
    deal with multiple classifications. We will cover them in the next step.


!!! example "Add a category"

    Add a category to your first blog post by adding it to the page header:

    ``` hl_lines="6 7""
    ---
    date: 2023-12-31
    updated: 2024-01-02
    authors:
      - material
    categories:
      - Holidays
    ---
    ```

    Now that the blog post has been categorised, the `Holidays` category appears
    under `Categories` in the main navigation and the blog post appears in the
    index page for this category.

Material allows you to control what categories can be used by declaring them in
the `mkdocs.yml`. This way you can make sure that authors stick to agreed
categories and that typos are detected.

!!! example "Control your categories"

    Add a `categories_allowed` entry to the configuration of the Blog plugin
    with the entries "Holidays" and "News":

    ```yaml hl_lines="5-7"
    plugins:
      - search
      - blog:
          authors_profiles: true
          categories_allowed:
            - Holidays
            - News
    ```

    Now, then you add a category to a blog post that does not match one of these
    two, you should get a build error. 

## 8. Using tags

The [Tags plugin] provides another way to classify blog posts and to make
them accessible independently of the main navigation structure. Tags are useful
for making related content easily discoverable even if it is in different parts
of the navigation hierarchy.

[Tags plugin]: https://squidfunk.github.io/mkdocs-material/plugins/tags/

You may have a tutorial, like this one, showcasing features, a more
comprehensive setup guide, as well as reference documentation. Adding the same 
tag to all three shows that they are related. As you will see, it is possible to
navigate from a page that is tagged to the tag index and, from there, to other
pages that carry the same tag.

!!! example "Enable the plugin"

    First, you need to add the plugin to your `mkdocs.yml`:

    ```yaml hl_lines="8"
    plugins:
      - search
      - blog:
          authors_profiles: true
          categories_allowed:
            - Holidays
            - News
      - tags
    ```

    Once this is done, you can 

## x. 
## X. Pagination 
## 

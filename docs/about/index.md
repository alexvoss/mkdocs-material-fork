# Introduction

Material for MkDocs is based on [MkDocs], a static site generator. Originally
conceived as a theme for MkDocs that took inspiration from Google's Material
Design, it has since grown to become a comprehensive solution for developing
technical documentation as well as other web content.

When starting to use Material for MkDocs, it is useful to first gain a 30,000ft
overview in order to understand how MkDocs and Material for MkDocs work together
and how you can also draw on a right pool of some 240 [plugins].

[plugins]: https://github.com/mkdocs/catalog

```mermaid
mindmap
  root(MkDocs)
    material("`**Material** for MkDocs`")
    ::: .mer-material
      plugins(Plugins)
        blog(Blog)
        grou(Group)
        info(Info)
        meta(Meta)
        offline(Offline)
        optimize(Optimize)
        privacy(Privacy)
        projects(Projects)
        search(Search)
        social(Social)
        tags(Tags)
        typeset(Typeset)
      trans(Translations)
    plugins2(Plugins)
      mkdocstrings(mkdocstrings)
      rss(mkdocs-rss-plugin)
    deps(Dependencies)
      markdown(Python Markdown)
      jinja(Jinja2)
    cust(Customization)
      css(Extra CSS)
      js(Extra JS)
      hooks(Hooks)
```

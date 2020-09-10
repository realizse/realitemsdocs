---
title: Special layouts overview
tags: [special_layouts]
keywords: layouts, information design, presentation
last_updated: July 3, 2016
summary: "This theme has a few special layouts. Special layouts include the JS files they need directly in the page. The JavaScript for each special layout does not load by default for every page in the site."
sidebar: ridoc_sidebar
permalink: ridoc_special_layouts.html
folder: ridoc
---


{% include note.html content="By \"layout,\" I'm not referring to the layouts in \_layouts in the project files. I'm referring to special ways of presenting information on the same \"page\" layout." %}

## FAQ layout

See {{site.data.ridoc_urls.ridoc_faq.link}} for an example of the FAQ format, which follows an accordion, collapse/expand format. This code is from Bootstrap.

## Knowledgebase layout

See {{site.data.ridoc_urls.ridoc_kb_layout.link}} for a possible layout for knowledge base articles. This layout looks for pages containing specific tags.

## Shuffle layout

If you want a dynamic card layout that allows you to filter the cards, see {{site.data.ridoc_urls.ridoc_shuffle.link}}. This uses the Shuffle JS library.

{% include links.html %}

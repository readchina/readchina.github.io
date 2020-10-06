---
layout: viz
title: ReadAct
description: Reading Act Database
nav-menu: true
show_tile: true
view:
  - view-name: view1a
    view-index: 0
  - view-name: view1b
    view-index: 1
  - view-name: view2
    view-index: 2
---

## {{ page.title }}: Introduction
[![DOI](https://zenodo.org/badge/96089230.svg)](https://zenodo.org/badge/latestdoi/96089230)

The *ReadAct* database was originally developed as part of the Worlds of Reading in China’s long 1970s research project [*Lesewelten*](http://www.sinologie.uni-freiburg.de/forschung/projecthenningsen). It is under active development as part of [*READCHINA*](https://readchina.github.io/). Here we gather pieces of analysis that our team has undertaken based on the *ReadAct* in an ongoing fashion.

*ReadAct* provides various interfaces for users to interact with its data. This page features a collection of graphical displays accompanied by short snippets of analysis. These views are updated automatically and reflect the latest stage of our ongoing work on *ReadAct*. It is therefore possible that the text and the visualization are not in perfect alignment. Should you note something odd, please let us know via the contact form. You can freely explore and interact with the views by selecting `Open in Vega Editor` from the menu button on any data visualization. The short data stories here provide a space for quick explorations based on our overarching research questions. For fuller analysis please consult the publications section of our homepage.

For more advanced means of interacting with our dataset, please follow the link above to our data repository, which contains a SQL database and additional tools for searching and mangling our data. To cite our dataset please use the DOI link at the top of this page, to generate a citation in accordance with your style requirements.

### High-level view of DB
At its core *ReadAct* implements a relational data model of individual reading acts. From this we derive a typology of reading (`reading-types`) such as: clandestine reading, collective reading, reading as performance, etc. Which connects the various agents and works. Whenever possible we try to record spatial information about the reading acts in question as well as specific bibliographical data about the publishing history of a given work. Because historical accounts of reading acts tend to be vague, we decided not to collects copy level bibliographical meta-data, but more general edition level data.  

Detailed technical documentation of the database schema, and information for developers will appear here soon.

### Network
Network analysis (sometime likened to the close study of fur balls) provides another means of analyzing and looking at the sum of all the acts captured in *ReadAct*. The following links discuss individual graphs and their interpretation:
-   [networks](./reading-acts.html) \[WIP\]
-   [E-R model](./db-schema.html) \[Coming soon\]

## Reading books (and more)
One of the first questions one might ask, is which books have been read during the cultural revolution? According to autobiographical accounts we can see that *The Water Margin* a novel about … was the most widely read novel.

<div id="view1a" class="viz"> </div>

Yet, reading can also take an extended sense, beyond the confines of literary works. We therefore took a closer look at other works of art, such as movies, paintings, or even music that was *read* according to the accounts of those remembering their life during the CR.

<div id="view1b" class="viz"> </div>

Side-by-side both queries show that the consumption of art, and reading in particular did (not?) adhere to …

### Popular authors
The previous views look at individual works, to determine popular creators, we need to group works belonging to the same author together. It should come as no surprise that Mao Zedong is the most popular creator of works being read within our data-set. However, looking at other popular choices, we see that next to Karl Marx (another usual suspect), Lu Xun and Alexandre Dumas are on equal footing.

<div id="view2" class="viz"> </div>

It seems that the classics, both Chinese and foreign, continued to be very popular in spite of revolutionary rhetoric.

## Conclusion
As the result of compiling *ReadAct* we often found ourselves extending the scope of what we considered *reading*. To our knowledge few systematic studies of different types of reading have been conducted and even fewer have tried to formalize their typology in the way we have done. It is our hope that this typology can serve as a useful example for other researchers interested in the history of reading.

Our research into the hermeneutic effects of different types of readings, the social composition of readers, the historical evolution of reading types, and the relation between works and reading types is ongoing. *ReadAct* encourages us to critically reflect our own conceptual framework and its cultural and historic specificity. Lastly, because of the collaborative nature of *ReadAct* we aim to arrive at a consistent conceptual model for different research foci. The cold logic of the machine, and its insistence on clear definition, thereby becomes a tool, to help us find new connections and test assumptions we might otherwise have missed.  

---
layout: viz
title: ReadAct
author: Lena Henningsen and Duncan Paterson 
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
  - view-name: view5a
    view-index: 4
  - view-name: view5b
    view-index: 5
  - view-name: view5c
    view-index: 6
---

## {{ page.title }}: Introduction
[![DOI](https://zenodo.org/badge/96089230.svg)](https://zenodo.org/badge/latestdoi/96089230)
<p style="text-align: right;">{{ page.author }}</p>

The *ReadAct* [database](https://github.com/readchina/ReadAct) was originally developed as part of the Worlds of Reading in China’s long 1970s research project [*Lesewelten*](http://www.sinologie.uni-freiburg.de/forschung/projecthenningsen). It is under active development as part of *READCHINA*. Here we gather pieces of analysis that our team has undertaken based on the *ReadAct* in an ongoing fashion.

*ReadAct* provides various interfaces for users to interact with its data. This page features a collection of graphical displays accompanied by short snippets of analysis. These views are updated automatically and reflect the latest stage of our ongoing work on *ReadAct*. It is therefore possible that the text and the visualization are not in perfect alignment. Should you note something odd, please let us know via the contact form. You can freely explore and interact with the views by selecting `Open in Vega Editor` from the menu button on any data visualization. The short data stories here provide a space for quick explorations based on our overarching research questions. For fuller analysis please consult the publications section of our homepage.

For more advanced means of interacting with our dataset, please follow the link above to our data repository, which contains a SQL database and additional tools for searching and mangling our data. To cite our dataset please use the DOI link at the top of this page, to generate a citation in accordance with your style requirements.

### High-level view of the database
At its core *ReadAct* implements a relational data model of individual reading acts. From this we derive a typology of reading (`reading-types`) such as: clandestine reading, collective reading, reading as performance, etc. which connects the various agents and works. Whenever possible we try to record spatial information about the reading acts in question as well as specific bibliographical data about the publishing history of a given work. Because historical accounts of reading acts tend to be vague, we decided not to collects copy level bibliographical meta-data, but more general edition level data.  

Detailed technical documentation of the database schema, and information for developers will appear here soon.

### Network
Network analysis (sometime likened to the close study of fur balls) provides another means of analyzing and looking at the sum of all the acts captured in *ReadAct*. The following links discuss individual graphs and their interpretation:
-   [networks](./reading-acts.html) \[WIP\]
-   [E-R model](./db-schema.html) \[Coming soon\]

## Reading books (and more)
As of spring 2021, the focus of the *ReadAct* database is on reading acts during the Cultural Revolution. The data was collated from a wide variety of autobiographical sources that record – to varying detail – what individuals, or groups of individuals, read during the Cultural Revolution. The sample consists of texts by 95 authors, of whom 71 are male, 17 are female, and for seven the gender could not be identified. These authors – most of them belonging to the generation of the educated sent-down youth (*zhishi qingnian* 知识青年 or *zhiqing* 知情) – record 1,054 reading acts, pointing to 415 identifiable authors and 234 concrete texts (fiction, non-fiction, poetry; Chinese and foreign; internal and open publication). The autobiographies were published within China and elsewhere, in print and online, between 1980 and 2016 (with the bulk of publications published after 1999), including both book-length autobiographies and shorter life-writing texts. While some of the reading acts described are cursory and may only hint at an author or a text, others are very elaborate providing us with detailed descriptions of the conditions of the reading act, an interpretation and an elaboration of the impact that a particular text – or sets of texts – may have had on an individual. Also, we define reading in a broad sense as the interaction of individuals with text, including, but not limited to, borrowing, discussing or copying a book, as well as actual reading. For a closer analysis of the concept of the reading act, please see [here](https://readchina.github.io/interventions/What_is.html).

The analysis of the data thus may begin with a question about the titles read most widely at the time. (Or, to be more precise, about the titles that appear most often in written accounts of the time). The data shows that *The Water Margin* (*Shuihuzhuan* 水浒传) one of the classics of premodern Chinese fiction was most widely read, followed by two non-fictional books, both translations from English: *The New Class* by Djilas, and *The Rise and Fall of the Third Reich* by Shirer, both of which were only available at the time as internal publication. In theory, these texts were only available to cadres of the CCP – ReadAct demonstrates how porous this system had become as these texts circulated widely. As you go through the chart below, you may see that the other widely read titles similarly stem from Chinese and non-Chinese authors; also, while some were officially endorsed, many others were forbidden at the time, or only circulating internally.

<div id="view1a" class="viz"> </div>

Yet, reading can also take an extended sense, beyond the confines of literary works. We therefore took a closer look at other works of art, such as movies, paintings, or even music that was *read* according to the accounts of those remembering their life during the CR.

<div id="view1b" class="viz"> </div>

The reading (or consumption) of other cultural products shows a similar pattern to the reading of “textual text”, as officially endorsed items were read side-by-side with others which were frowned upon, or condemned at the time (as, for example, *The Butterfly Violin Concerto*).

### Reading acts with autobiography sources
(The following chart: reading acts whose source has an "autobiography" source.)
<div id="view5a" class="viz"> </div>

### Reading acts with science fiction sources
(The following chart: reading acts whose source has an "science fiction" source.)
<div id="view5b" class="viz"> </div>

### Reading acts with fictional sources
(The following chart: reading acts whose source has a genre_type "fiction".)
<div id="view5c" class="viz"> </div>

### Popular authors
The previous views look at individual works, to determine popular creators, we need to group works belonging to the same author together. It should come as no surprise that Mao Zedong is the most popular creator of works being read within our data-set. However, looking at other popular choices, we see that next to Karl Marx (another usual suspect), Lu Xun and Alexandre Dumas are on equal footing.

<div id="view2" class="viz"> </div>

It seems that the classics, both Chinese and foreign, continued to be very popular – and that works that were officially labeled as “poisonous weeds” proved to be particularly inspiring reads, in spite of Cultural Revolutionary rhetoric.

## Conclusion
As the result of compiling *ReadAct* we often found ourselves extending the scope of what we considered *reading*. To our knowledge few systematic studies of different types of reading have been conducted and even fewer have tried to formalize their typology in the way we have done. It is our hope that this typology can serve as a useful example for other researchers interested in the history of reading.

Our research into the hermeneutic effects of different types of readings, the social composition of readers, the historical evolution of reading types, and the relation between works and reading types is ongoing. *ReadAct* encourages us to critically reflect our own conceptual framework and its cultural and historic specificity. Lastly, because of the collaborative nature of *ReadAct* we aim to arrive at a consistent conceptual model for different research foci. The cold logic of the machine, and its insistence on clear definition, thereby becomes a tool, to help us find new connections and test assumptions we might otherwise have missed. 

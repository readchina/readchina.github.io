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

The analysis of the data thus may begin with a question about the titles read most widely at the time. (Or, to be more precise, about the titles that appear most often in written accounts of the time). The data – as assembled in June 2023 – shows that *Le Comte de Monte-Cristo* and *The Water Margin* (*Shuihuzhuan* 水浒传) one of the classics of premodern Chinese fiction were most widely read, followed by fictional and non-fictional books, translations from various foreign languages: *The New Class* by Djilas, *Jean-Christophe* by Romain Rolland, *How the Steal was Tempered* by Ostrovski, and Marx’ *Das Kapital*, of which some were only available at the time as internal publications. In theory, these texts were only available to cadres of the CCP – ReadAct demonstrates how porous this system had become as these texts circulated widely. As you go through the chart below, you may see that the other widely read titles similarly stem from Chinese and non-Chinese authors; also, while some were officially endorsed, many others were forbidden at the time, or only circulating internally.

<div id="view5a" class="viz"> </div>

Yet, reading can also take an extended sense, beyond the confines of literary works. We therefore took a closer look at other works of art, such as movies, paintings, or even music that was *read* according to the accounts of those remembering their life during the CR.

<div id="view1b" class="viz"> </div>

The reading (or consumption) of other cultural products shows a similar pattern to the reading of “textual text”, as officially endorsed items were read side-by-side with others which were frowned upon, or condemned at the time (as, for example, *The Butterfly Violin Concerto*).

### Popular authors
The previous views look at individual works, to determine popular creators, we need to group works belonging to the same author together. It should come as no surprise that Mao Zedong is the most popular creator of works being read within our data-set. However, looking at other popular choices, we see that next to Karl Marx (another usual suspect), Lu Xun and Alexandre Dumas are on equal footing.

<div id="view2" class="viz"> </div>

It seems that the classics, both Chinese and foreign, continued to be very popular – and that works that were officially labeled as “poisonous weeds” proved to be particularly inspiring reads, in spite of Cultural Revolutionary rhetoric.

### Reading Acts in Chinese Fictional Texts
The ReadAct database also can be used to make enquiries about reading acts in fictional texts. After all, fictional characters may enjoy reading as much as their real-world counterparts. Reading can be an efficient tool to characterize persons and to situate them socially, culturally, politically and ideologically. It comes as no surprise then, that Chinese novels and short stories contain many scenes in which the characters read. Reading acts in fictional texts are similar to those in autobiographical sources, yet the fictional status of the texts brings with it a number of constraints that the data model needs to take into account: A fictional character may read a book which exists in the real-world, or one that the author invented alongside with the character. And, moreover, a fictional text may describe a fictionalized version of a person who exists in the real world – yet, describing that person as reading a distinct text may hold different truth values than one that a similar scene in a life-writing text describes. A fictional Mao Zedong may be reading Harry Potter; the real-world Mao Zedong clearly never read the text, for reasons of ideological conviction as much as because of the constraints of temporal succession: Harry Potter was published decades after the death of Mao. To account for these constraints in the data model, we differentiate reading acts according to the text in which they occur. Our – to date (June 2023) still very limited sample of texts – thus shows The Gadfly as the most popular title:

<div id="view5c" class="viz"> </div>

This, however, has to do with the fact that the sample consists of a number of SF stories, of three stories by Ah Cheng and of the scar literature short story “The Class Teacher” (班主任 by Liu Xinwu 刘心武). And throughout this latter story, the characters discuss the novel, its contents and its ideological implications ([Henningsen 2020](https://www.researchgate.net/publication/342521654_POACHING_WORLD_LITERATURE_IN_CHINA%27S_LONG_1970s_Asian_Journal_of_African_Studies#fullTextFileContent)). So, while *The Gadfly* definitely was an important literary text in Maoist China, the graph exaggerates its importance. Therefore, in a next step, we narrow down the reading acts to those which occur in the science fiction stories in the sample. Of the vast literary output of Chinese SF in recent years, this sample is taken from a number of SF novels and anthologies of SF translated into foreign languages (English, German) over the past decades, thus containing a small sample of texts from the first post-Maoist wave of science fiction and a somewhat more substantial sample of more recent texts, when not only SF is blossoming in China, but also finding interested readers abroad. Once again, this does not represent all SF ever written in China, but a slightly larger sample that allows drawing a few conclusions.

<div id="view5b" class="viz"> </div>

Rachel Carson’s *The Silent Spring* is boasting most records as it is read several times in Liu Cixin’s famous novel *The Three Body Problem*. Other than that, we can see that readers in Chinese SF read a wide scope of world literature, ranging from the *Iliad* to *1984* or Douglas Adams’ *The Restaurant at the End of the Universe*, as well as Chinese texts ranging from *The Journey to the West* to Lu Xun’s “Diary of a Madman”. With reading acts and other intertextual references, Chinese SF thus clearly positions itself within the canon of world literature and emphasizes its own literary status.
 
Of course, the data from autobiographical and fictional sources can also be included into the same graph:

<div id="view1a" class="viz"> </div>

Given that this graph combines sources from different times and – for the fictional texts – a sample that is anything but representative, the explanatory value of this graph is limited. After all, *The Gadfly* clearly cannot be seen as the text most widely in China. However, this record may remind us of the fact that at a certain point in Chinese history (throughout the Mao years and into the early post-Mao years), it definitely was an important text. After all, of the 20 mentions here, 16 relate to “The Class Teacher” – and the remaining for to autobiographical texts about the 1970s.


## Conclusion
As the result of compiling *ReadAct* we often found ourselves extending the scope of what we considered *reading*. To our knowledge few systematic studies of different types of reading have been conducted and even fewer have tried to formalize their typology in the way we have done. It is our hope that this typology can serve as a useful example for other researchers interested in the history of reading.

Our research into the hermeneutic effects of different types of readings, the social composition of readers, the historical evolution of reading types, and the relation between works and reading types is ongoing. *ReadAct* encourages us to critically reflect our own conceptual framework and its cultural and historic specificity. Lastly, because of the collaborative nature of *ReadAct* we aim to arrive at a consistent conceptual model for different research foci. The cold logic of the machine, and its insistence on clear definition, thereby becomes a tool, to help us find new connections and test assumptions we might otherwise have missed. 


## References
Henningsen, Lena 2020: “Poaching World Literature in China’s Long 1970s”, in: Asian Journal of African Studies 48, 119-149.

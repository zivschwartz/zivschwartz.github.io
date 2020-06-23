---
title: "Comparing and Contrasting the Content of US Presidential Inaugural Addresses and UK Political Party Manifestos from World War II to Present Day"
date: 2020-05-08
excerpt: "Examining the difference in how prominent political figures and parties from the United States and the United Kingdom use official addresses and manifestos.<br/><img src='/images/TADEntropy.png' style='width:395px;height:254px;'>"
collection: portfolio
---

## Summary

The purpose of this paper is to compare and contrast how prominent political figures and parties from the United States and the United Kingdom use official addresses and manifestos. The goal of this analysis will be to elucidate if historical and political circumstances impact these documents. Different metrics will be used to help understand how these official documents have adapted over time and how leaders and governments from two prominent world leaders compare. The analysis will focus on documents dating back to the end of World War II all the way through to the present day. Analysis done in R Studio.

Report can be found [here](https://github.com/zivschwartz/Inaugural_Address_vs_Manifestos/blob/master/TAD_Project.pdf), and relevant code can be found [in this GitHub repo](https://github.com/zivschwartz/Inaugural_Address_vs_Manifestos/blob/master/Project.Rmd).

**Data and Methods** 

The data used in this paper is readily available in Quanteda. The following quantitative metrics are performed in order to get a better textual understanding of the documents: Document Feature Length, Entropy, Type-to-Token Ratio (TTR), Moving Average Type-to-Token Ratio (MATTR), Yule's Characteristic K, and Cosine Similarity.

<p align="center">
  <img width="485.5" height="381" src="/images/TADLength.png">
</p>

The first major distinction is noting that the political manifestos are much longer than inaugural addresses. Each document serves a different purpose in the political world. Inaugural addresses are meant to present a concise vision for a president’s administration and goals for the country. Thus a shorter length is expected as they are read aloud to the entire country. On the other hand, the manifestos are focused on attracting voters, therefore requiring a deeper dive into policies and platforms for the party. 
 
 <p align="center">
  <img width="330" height="330" src="/images/TADEntropy.png">
</p>

The next metric used is entropy, a measure that holds the ability to give a reading on how much information is present in a document. The inaugural addresses from 1945 to 2017 have an entropy that hovers around 9 whereas the party manifestos have greater entropy, reaching a peak in 1979 of right around 11 and generally between 10 and 11. This again follows the expectation of the assumptions that underlie the differences in the documents.

 <p align="center">
  <img width="330" height="330" src="/images/TADLexComp.png">
</p>

Following this, the lexical complexity of each document is calculated using three different metrics: TTR, MATTR, and Yule’s Characteristic K. The simplest and most common metric for vocabulary richness is TTR, which calculates the ratio of unique words over total words in a document. Looking at Yule’s Characteristic K, it seems that UK manifestos decrease in lexical complexity over time, yet inaugural addresses do not follow the same trend, with peaks in 1953 and 2005.

 <p align="center">
  <img width="330" height="330" src="/images/TADSimilarity.png">
</p>

Finally, a similarity metric is used to see how closely inaugural addresses relate to either the conservative or labour manifestos. From the table, 75% of the addresses have a higher cosine similarity to the Conservative Party manifestos. The hypothesis presented earlier speculates that republican presidents would be expected to have a higher similarity to Con- servative Party manifestos and democratic presidents would have a higher similarity to the Labour Party manifestos, however this is not generally the case. 




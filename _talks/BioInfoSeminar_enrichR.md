---
title: "Enrichment Analysis with *enrichr*; What to be Aware of"
collection: talks
type: "Seminar"
permalink: /talks/BioInfoSeminar_enrichR
venue: "Department of Biomedicine, University Hospital Basel, University of Basel"
date: 2022-09-06
location: "Basel, Switzerland"
---

Contribution in the internal Bioinformatics seminar at the Department of Biomedicine.

In this talk I wanted to raise awarness to the details of enrichment analysis with Fisher's test as performed by popular [enrichr](https://maayanlab.cloud/Enrichr/) web service. Main message is that enrichr does not allow to upload user's own set of background genes (i.e. *universe*). Apparently the universe is chosen to be quite extensive, thus it may lead to a general shift of p-values towards more significant values.

<iframe src="/files/BioInfo_Sem_enrichR.pdf" width="100%" height="600px">
    Your browser does not support PDFs. 
    <a href="/files/BioInfo_Sem_enrichR.pdf">Download Presentation</a>
</iframe>
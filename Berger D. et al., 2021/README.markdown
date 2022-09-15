## The paper
### Whole-genome sequencing of Schistosoma mansoni reveals extensive diversity with limited selection despite mass drug administration
#### Duncan J. Berger, Thomas Crellen, Poppy H. L. Lamberton, Fiona Allan, Alan Tracey, Jennifer D. Noonan, Narcis B. Kabatereine, Edridah M. Tukahebwa, Moses Adriko, Nancy Holroyd, Joanne P. Webster, Matthew Berriman & James A. Cotton
---
Control and elimination of the parasitic disease schistosomiasis relies on mass administration of praziquantel. Whilst these programmes reduce infection prevalence and intensity, their impact on parasite transmission and evolution is poorly understood. Here we examine the genomic impact of repeated mass drug administration on *Schistosoma mansoni* populations with documented reduced praziquantel efficacy. We sequenced whole-genomes of 198 *S. mansoni* larvae from 34 Ugandan children from regions with contrasting praziquantel exposure. Parasites infecting children from Lake Victoria, a transmission hotspot, form a diverse panmictic population. A single round of treatment did not reduce this diversity with no apparent population contraction caused by long-term praziquantel use. We find evidence of positive selection acting on members of gene families previously implicated in praziquantel action, but detect no high frequency functionally impactful variants. As efforts to eliminate schistosomiasis intensify, our study provides a foundation for genomic surveillance of this major human parasite.

## Using WormBase ParaSite

In this paper, the researchers examine the genomic impact of repeated mass drug administration on *Schistosoma mansoni* populations with documented reduced praziquantel efficacy.

They collected samples from regions in Uganda with different exposure to praziquantel and performed whole genome sequencing to explore how schistosome populations change in response to repeated MDA as well as to monitor for the potential emergence and spread of praziquantel resistance.

Let's try to follow the same steps that these researchers used to perform their analysis using WormBase ParaSite.
---

# Tasks
### Reference genome download
The researchers had to download The *S. mansoni* reference genome (v.7) from WormBase Parasite to perform their genomic analyses.

**Task 1: Can you find out how to download data from WormBase ParaSite?**

<details closed>
<summary>Hint</summary>
You can download data from WormBase ParaSite using our Downloads page (https://parasite.wormbase.org/ftp.html)<br>
1. Go to WormBase ParaSite (https://parasite.wormbase.org/)<br>
2. Click "Downloads" at the top menu.<br>
3. In the middle of the page you can find a table with genomes and their FTP links. Search for "mansoni" in the filter text box at the top right corner of the table.<br>
5. You can use the links appeared for S. mansoni to download the reference genome from our FTP server.<br>
</details>

---
### Annotating genomic regions
Following population genomic analyses, researchers identified a list of genomic regions as being under strong selection in Mayuge where we expect selection for survival following praziquantel treatment to be strongest.

These genomic regions are:<br/>
SM_V7_1:3718001:3846001<br/> 
SM_V7_1:22000001:22052001<br/>
SM_V7_2:2624001:2756001<br/>
SM_V7_2:3434001:4806001<br/>
SM_V7_2:31552001:31566001<br/>
SM_V7_2:31874001:32472001<br/>
SM_V7_2:43554001:43836001<br/>
SM_V7_2:45248001:45450001<br/>
SM_V7_2:46084001:46580001<br/>
SM_V7_2:47004001:48088001<br/>
SM_V7_3:332001:498001<br/>
SM_V7_3:38176001:38342001<br/>
SM_V7_4:2168001:2732001<br/>
SM_V7_4:5108001:5118001<br/>
SM_V7_4:18898001:20024001<br/>
SM_V7_4:21128001:21146001<br/>
SM_V7_5:17006001:17360001<br/>
SM_V7_5:17718001:17840001<br/>
SM_V7_5:20342001:20354001<br/>
SM_V7_7:1604001:1684001<br/>
SM_V7_7:11236001:11294001<br/>
SM_V7_7:13326001:13656001<br/>
SM_V7_ZW:42001:196001<br/>
SM_V7_ZW:6934001:7172001<br/>
SM_V7_ZW:80928001:81030001<br/>

**Task 2: Can you find what genes can be found in the above regions using WormBase ParaSite's BioMart tool?**

This paper is using an older *S. mansoni* assembly, so please use use the archived WormBase ParaSite 16 website (https://release-16.parasite.wormbase.org/) which has this older assembly.

<details closed>
<summary>Hint</summary>
1. Go to WormBase ParaSite archive 16 (https://release-16.parasite.wormbase.org/)<br>
2. Click "BioMart" at the top menu.<br>
3. Select the "Schistosoma mansoni PRJEA36577" species in the SPECIES tab.<br>
4. Paste the above genomic coordinates into the "Multiple regions (Chr:Start:End:Strand)" dialog box under the REGION tab.<br>
5. Click on the Output Attributes and customise your output data/format (make sure to have "Gene Stable ID" clicked under "Gene attributes").<br>
6. Click "Results", when you are done customising, to see the output table.<br>
</details>

Perform gene set enrichment analysis on the gene-set we got from BioMart:

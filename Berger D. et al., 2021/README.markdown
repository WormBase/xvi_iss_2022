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

### Reference genome download
The researchers had to download The *S. mansoni* reference genome (v.7) from WormBase Parasite to perform their genomic analyses.

#### Task 1: Browse and Download *S. mansoni*'s reference genome from WormBase ParaSite

#### Task 1a: Browse the genome list of WormBase ParaSite and S. mansoni genome statistics.

<details closed>
<summary>Solution</summary>
1. Go to WormBase ParaSite (https://parasite.wormbase.org/).<br><br>
2. Click ”Genome List" at the top menu.<br><br>
3. Use the Show/hide column at the top of the table to display more genome statistics for each genome.<br><br>
4. Hover your mouse pointer over the BUSCO ANNOTATION and BUSCO ASSEMBLY pie charts to reveal the BUSCO metrics for each genome.<br><br>
5. Click on Schistosoma mansoni to open its genome landing page. There you can find information about the genome and useful assembly/annotation statistics.<br><br>
---
</details>

#### Task 1b: Download S. mansoni's reference genome from WormBase ParaSite.

<details closed>
<summary>Solution</summary>
You can download data from WormBase ParaSite using our Downloads page (https://parasite.wormbase.org/ftp.html)<br><br>
1. Go to WormBase ParaSite (https://parasite.wormbase.org/)<br><br>
2. Click "Downloads" at the top menu.<br><br>
3. In the middle of the page you can find a table with genomes and their FTP links. Search for "mansoni" in the filter text box at the top right corner of the table.<br><br>
5. You can use the links appeared for S. mansoni to download the files you need.<br><br>
6. To download the reference genome click on the FASTA button under the "Genomic" column for S. mansoni and a download will automatically start.<br><br>

Alternatively, you can directly browse our FTP server here: https://ftp.ebi.ac.uk/pub/databases/wormbase/parasite/releases/
</details>

---
### Gene pages
The researchers write: "The strongest signals of selection were detected within chromosome 2 regions ... Within one of these regions we identified a single locus (47.06–47.34 Mb) containing four sodium/potassium/calcium exchanger proteins (Smp_170450, Smp_336070, Smp_328710, Smp_094390) ... ".

After they discovered these important genes, researchers might want to investigate some basic information about their function, location, sequences etc. WormBase ParaSite's gene pages contain all these information that the researchers might find useful.

#### Task 2: Navigate to the gene page of one of the genes mentioned by the researchers. Try to find information about the gene's function, transcripts, its UniProt ID and its genomic/protein sequences.

#### Task 2a: Find general gene information (name, description, how many transcripts etc).
<details closed>
<summary>Solution</summary>
1. Go to WormBase ParaSite (https://parasite.wormbase.org/).<br><br>
2. Paste the Gene ID (i.e. Smp_336070) in the search box at the top right corner of the page and press Enter.<br><br>
3. The search will return the gene entry you searched for. Click on the Gene ID to open up the corresponding gene page.<br><br>
4. You're on the gene page. Use the menu on your left to navigate.<br><br>
</details>
You can learn more about the gene pages here (https://parasite.wormbase.org/info/Browsing/gene_pages.html).<br><br>

#### Task 2b: Use the “Region in detail” to visualise the gene in our genome browser. Do the same with Jbrowse.
<details closed>
<summary>Solution</summary>
1. While on the gene page, click on the "Region in detail" button under the "Genomic context" header.<br><br>
2. You can now browse the gene's location using the genomic browser. Use your mouse to navigate around the gene and hover over different features of the gene to see more information.<br><br>
3. Reverse strand is visible while UTRs are also annotated.<br><br>
4. You can use the "Configure tracks" button at the top left of the browser to load more tracks in the view.<br><br>
5. You can use "Add RNAseq tracks" or "Add custom tracks".<br><br>
6. You can learn more about the Genome Browser here (https://parasite.wormbase.org/info/Browsing/genome_browser_ensembl.html).<br><br>
<br>
Using Jbrowse:<br>
7. Click on the top-right "View region in Jbrowse" button to visualise the same region in a different genome browser called Jbrowse.<br><br>
8. You are being redirected to Jbrowse. When Jbrowse loads use your mouse to navigate around the gene and find nearby genes. Click on the gene models to see more information.<br><br>
9. Use the "Select tracks" at the top-left of the browser and select a few tracks to add to the view.<br><br>
10. You can also load your own tracks by clicking "Track"->"Open track file or URL" from the top menu.<br><br>
11. To learn more about Jbrowse visit our help page here (https://parasite.wormbase.org/info/Browsing/genome_browser_jbrowse.html).<br><br>

Tip: Jbrowse is also accessible via a button in [WormBase ParaSite genome list](https://parasite.wormbase.org/species.html) and the [genome's landing page](https://parasite.wormbase.org/Schistosoma_mansoni_prjea36577).
</details>

#### Task 2c: Find the genomic/protein sequence for this gene.
<details closed>
<summary>Solution</summary>
1. While on the gene page, click the "Sequence" on the left "Gene-based displays" menu.<br><br>
2. Scroll down and you will see the "Marked-up sequence" for this gene. This is the genomic sequence for this gene. You can download it or Blast it using the buttons above the sequence.<br><br>
3. Similarly, to find its protein sequence you need to first go to a gene's trascript page. To do that, click on a trascript ID in the trascript table (above the "Marked-up sequence" header).<br><br>
4. You can then use the left "Transcript-based displays" menu to view the sequences of the Exons, cDNA and Protein for this transcript.<br><br>
</details>

#### Task 2d: Explore the protein domains, features and AlphaFold 3D model of the encoded protein.
<details closed>
<summary>Solution</summary>
1. Information about protein domains & features are available at the transcript page. To go to a transcript page you need to click on a transcript ID in the transcript table.<br><br>
2. On the left "Transcript-based displays" menu, click on "Domains & features".<br><br>
3. Use the tables to discover which domains and features have been annotated in this gene's protein.<br><br>
4. On the left "Transcript-based displays" menu, click on the "AlphaFold predicted model".<br><br>
5. Use the "AlphaFold predicted model" widget to discover the 3D protein structure of the protein.<br><br>
6. Use your mouse (drag/drop) to move and rotate the protein. You can zoom/unzoom using your mouse wheel.<br><br>
7. Use the right side menu to show/hide different protein/gene features (e.g. "Exons","PANTHER","Pfam" etc).
</details>

#### Task 2e: Find orthologues for this gene in other Schistosoma species.

Wait! What orthologues and paralogues are? Read [here](https://sciencing.com/different-variants-gene-called-8092322.html) and/or [here](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2001-2-8-interactions1002) to find more!

<ins>In a nutshell</ins><br>
**Orthologues**: Genes which evolved from a common ancestral gene by speciation that usually have retained a similar function in different species.<br>
**Paralogues**: Paralogs are homologous genes that arise from gene duplication events. Their common ancestry and replicated sequence often leads to similar structure and function in related pathways and protein complexes.<br>

<ins>Why would researchers want to find orthologues in other species for their gene of interest?</ins> Function Annotation! If the function of this gene in S. mansoni is not known, you can check the function of its orthologues genes in other species like C. elegans or other Schistosomas. Many times you will find that orthologous genes function will be similar to this of your gene of interest.

<details closed>
<summary>Solution</summary>
1. While on the gene page, click "Orthologues" on the left "Gene-based displays" menu under "Comparative genomics".<br><br>
2. We need to wait a little bit for the orthologues to load.<br><br>
3. When loaded, two tables are visible: "Summary of orthologues of this gene" and "Selected orthologues".<br><br>
4. On the left "Summary of orthologues of this gene" menu, you can select to display orthologues for one or more taxonomic groups (nematodes, platyhelminths)".<br><br>
5. The second table shows the list of orthologues found for this gene.<br><br>
6. You can use the search box at the top right to filter orthologues just for schistosoma species by typing "schistosoma".<br><br>
7. Use the three buttons in the "Compare" column: "Alignment (protein)", "Alignment (cDNA)" and "Gene Tree (image)" to further explore the comparison.<br><br>
8. Click on the "Gene Tree (image)" of one of the orthologues in the list, to explore the gene tree for the specific orthologue.<br><br>
9. You can follow the same instructions to discover paralogues too!<br><br>
</details>

#### Task 2f: Explore phenotypes associated with the gene of interest.
<details closed>
<summary>Solution</summary>
1. While on the gene page, click "Phenotypes" on the left "Gene-based displays" menu.<br><br>
2. We need to wait a little bit for the phenotypes to load.<br><br>
3. When loaded, two tables are visible: "Phenotypes associated with this gene" and "Phenotype, disease and trait annotations associated orthologues of this gene in other species".<br><br>
4. In the first "Phenotypes associated with this gene" table, you can find a list of phnoetypes, diseases and traits associated directly with this gene for this species, based on experimental evidence. If there are no associate phenotypes for your gene in the first table, a message showing "None Found" will be displayed. You can try and work with a different gene (i.e. Smp_025260) which has phenotype associations. Literature evidence for each association can be found under the "Study" column.<br><br>
5. The second table shows phenotype, disease and trait annotations associated orthologues of this gene in other species. Usually, there are not many phenotypic data available for parasitic worms, for this reason exploring phenotypes associated with other species like **C. elegans** is really useful for scientists. You can use the links in the table to navigate to the orthologous gene in the other species and find more information there.<br><br>
6. Gene-phenotype association links can also be found in our [Downloads FTP server](https://ftp.ebi.ac.uk/pub/databases/wormbase/parasite/releases/). Look for the files ending in ".phenotypes.gaf.gz"  and ".orthology-inferred_phenotypes.gaf.gz".<br><br>
</details>

#### Task 2g: Explore papers mentioning your gene of interest.
<details closed>
<summary>Solution</summary>
1. While on the gene page, click "Literature" on the left "Gene-based displays" menu.<br><br>
2. When loaded, a "Literature" table is visible. It lists the "Pubmed ID", "Title", "Authors" and "Journal" of all papers in EuropePMC about S. mansoni that mention your gene of interest.<br><br>
</details>

---
### Multiple querying 
So far we have seen how you can manually browse [WormBase ParaSite](https://parasite.wormbase.org/) by searching for genes and then navigating to their gene/transcript/protein pages. However, in many cases you might have to automatically extract information from [WormBase ParaSite](https://parasite.wormbase.org/) for multiple entries. Or simply you might need to extract information about your favourite genome's features that fullfil some criteria.<br>
<br>
[WormBase ParaSite's BioMart](https://parasite.wormbase.org/biomart/martview/) enables you to perform multiple queries like that as it is an easy-to-use web-based tool that allows extraction of data without any programming knowledge or understanding of the underlying database structure.

**Back to our paper**, following population genomic analyses, researchers identified a list of genomic regions as being under strong selection in Mayuge where we expect selection for survival following praziquantel treatment to be strongest!

These genomic regions are:<br>
SM_V9_1:3632837:3639271<br>
SM_V9_1:21187604:21191656<br>
SM_V9_2:789524:808207<br>
SM_V9_2:1363187:1803756<br>
SM_V9_2:1989837:2487785<br>
SM_V9_2:2654327:2751763<br>
SM_V9_2:29260243:29265542<br>
SM_V9_2:29603956:30139764<br>
SM_V9_2:30283551:30292597<br>
SM_V9_2:41232814:41453191<br>
SM_V9_2:42919049:43059968<br>
SM_V9_2:43704893:44183538<br>
SM_V9_2:44626967:45569668<br>
SM_V9_3:2410066:2411710<br>
SM_V9_3:37706186:37810830<br>
SM_V9_4:2156993:2619275<br>
SM_V9_4:5009688:5010602<br>
SM_V9_4:18557189:19024742<br>
SM_V9_4:19161079:19304157<br>
SM_V9_5:16214354:16374531<br>
SM_V9_5:16813158:16866668<br>
SM_V9_5:19360379:19363334<br>
SM_V9_7:1587530:1648411<br>
SM_V9_7:11174239:11191391<br>
SM_V9_7:13266191:13494236<br>
SM_V9_PAR1:59785:195092<br>
SM_V9_PAR2:36554914:36616990<br>

#### Task 3: Identify all the genes that can be found in the above genomic regions using WormBase ParaSite's BioMart tool

<details closed>
<summary>Solution</summary>
1. Go to WormBase ParaSite (https://parasite.wormbase.org/).<br><br>
2. Click "BioMart" at the top menu. You're now on BioMart's page! Filters and attributes can be selected in the right panel. A summary of your choices is also displayed in the left panel.<br><br>
BioMart allows you to restrict your query with information that you know, e.g: species, input a list of IDs, restrict to a region. You can access the filter page by clicking on the "1. Query Filters" button located on the left panel. Filters are organised into different sections, clicking on the "+/-" boxes will expand/collapse a section and display its content.<br><br>
3. Expand the "SPECIES" section by clicking on the "+" box on the right panel. Select the "Schistosoma mansoni PRJEA36577" species in the SPECIES tab.<br><br>
4. Expand the "REGION" section by clicking on the "+" box on the right panel. Then, paste the above genomic coordinates into the "Multiple regions (Chr:Start:End:Strand)" dialog box.<br><br>
5. Click on the "2. Output Attributes" button on the left panel.<br><br>
By clicking on the "2. Output Attributes" button on the left panel, you will access the mart attribute page. This page allows you to select your desired output; the default output is "Genome project" and "Gene stable ID" in the WormBase ParaSite mart. The attributes are organised in pages that you can access by selecting the radio buttons at the top of the right panel.<br><br> 
6. Expand the "SPECIES AND GENOME INFORMATION" by clicking on the "+" box on the right panel. Then deselect the "Genome project" field. We don't want it in our final table.<br><br>
7. Expand the "GENE" section by clicking on the "+" box on the right panel. Then make sure that only the "Gene stable ID" field is selected.<br><br>
8. Click on the "Results" button at the top-left of the screen. This will bring you to the result page.<br><br>
This page will, by default, show you a preview of the first 10 results of your query in HTML format. The number of results previewed and format can be changed by the View settings above the results preview table. You can also automatically remove all the duplicated results from your query by clicking on the "Unique results only" button. If you are happy with your query, you can use the "Export all results to" section at the top of the right panel to download your results.<br><br>
9. At the top of the right panel use the dropdown menu to select: "Export all results to File" and then "TSV". Tick the "Unique results only". Then click the "Go" button. A mart_export file will be automatically downloaded. It contains a list with all the genes that exist in the genomic regions the researchers identified.<br><br>
</details>
You can find more about BioMart [here](https://parasite.wormbase.org/info/data/biomart/index.html).
BioMart video Tutorial [here](https://www.ensembl.org/Multi/Help/Movie?db=core;id=189).

---
### Explore gene function with BioMart

Using BioMart, we managed to come up with the list of genes that might play a role in the survival following praziquantel treatment.

Now, we need to further explore the function of these genes as we did in Task 2. However, now we will extract all the necessary information researchers might find useful for all genes at once, using BioMart!

**Task 4. Find out more information about the function of the genes you identified in Task 3, using [WormBase ParaSite's BioMart tool](https://parasite.wormbase.org/biomart/martview/).**
<details closed>
<summary>Solution</summary>
1. Go to [WormBase ParaSite](https://parasite.wormbase.org/)<br><br>
2. Click "BioMart" at the top menu.<br><br>
3. Expand the "SPECIES" section by clicking on the "+" box on the right panel. Select the "Schistosoma mansoni PRJEA36577" species in the SPECIES tab.<br><br>
4. Expand the "GENE" section by clicking on the "+" box on the right panel. Then, paste the list of Gene IDs from Task 3 into the "ID list limit" dialog box and make sure the the tick box on the left of "Id list limit" is ticked. Similarly, tick the "Gene type" tick box and select "Protein Coding" to limit your results to protein coding genes.<br><br>
5. Click on the "2. Output Attributes" button on the left panel.<br><br>
6. Expand the "SPECIES AND GENOME INFORMATION" section by clicking on the "+" box on the right panel. Then deselect the "Genome project" field. We don't want it in our final table.<br><br>
7. Expand the "GENE" section by clicking on the "+" box on the right panel. Then select "Gene stable ID", "Chromosome/scaffold name", "Gene name", "Gene description" and "Transcript count" and all other fields you believe might be useful for our research.<br><br>
8. Expand the "EXTERNAL DATABASE REFERENCES AND ID CONVERSION" section by clicking on the "+" box on the right panel. Then select "UniProtKB/SwissProt ID".<br><br>
9. Expand the "GENE ONTOLOGY (GO)" section by clicking on the "+" box on the right panel. Then select "GO term accession", "GO term name".<br><br>
10. Expand the "INTERPRO PROTEIN DOMAINS" section by clicking on the "+" box on the right panel. Then select "InterPro ID", "InterPro short description".<br><br>
11. You can also expand the "OTHER PROTEIN DOMAINS" section and select more sources if you want.<br><br>
12. Expand the "ORTHOLOGUES" section by clicking on the "+" box on the right panel. Then navigate to the "Caenorhabditis elegans (PRJNA13758) [WS282] Orthologues" and select "Caenorhabditis elegans (PRJNA13758) [WS282] gene stable ID" and "Caenorhabditis elegans (PRJNA13758) [WS282] gene name".<br><br>
13. Click on the "Results" button at the top-left of the screen.<br><br>
14. At the top of the right panel use the dropdown menu to select: "Export all results to File" and then "TSV". Tick the "Unique results only". Then click the "Go" button. A mart_export file will be automatically downloaded. It contains a comma-separated file you can load in Excel and perform your desired analysis/filtering etc.<br><br>
</details>
You can find more about BioMart [here](https://parasite.wormbase.org/info/data/biomart/index.html).
BioMart video Tutorial [here](https://www.ensembl.org/Multi/Help/Movie?db=core;id=189).

## Genes and Genomes  <a name="genes_and_genomes"></a>

Throughout this course, we assume that you're familiar with genes and genomes. 

### Genes: the basics  <a name="basics_genes"></a>

A **gene** is a unit of the genome, a DNA sequence, that is transcribed into an RNA molecule, or a transcript. A gene's transcript may go on to be translated into a protein (in that case it is an mRNA), or it may have a role as a non-coding RNA. Examples of the latter include ribosomal RNAs (rRNA), transfer RNAs (tRNA) and microRNAs (miRNA).

In eukaryotes, most protein-coding genes comprise alternating **exons** and **introns** (some genes have a single exon), flanked by **untranslated regions** (UTRs). The exons constitute the parts of the gene that are translated into a polypeptide. Introns are transcribed but soon after excised and the final mature mRNA is formed by a 5’UTR, joined exons and a 3’UTR. A CAP and poly-A tail are added to the 5’ and 3’ ends respectively. These structures are essential to guarantee the molecular stability and downstream processing of the mRNAs.

![](figures/figure_3.0.5.png)

This figure represents the steps that are needed to transform information encoded in the DNA into a polypeptide and eventually a functional protein. The starting information is encoded in the genome. A gene encodes, among other things, the transcription start and transcription end. These are the nucleotides from where an RNA copy of the DNA will be generated. This copy is the pre-mRNA which is formed by exons and introns. Maturation of the mRNA molecule happens as it is transcribed and involves the splicing (removal) of introns with the concomitant joining of exons, addition of a CAP at the 5’ end and a polyadenylation tail (many As - AAAAAAA) at the 3’end. A processed mRNA will be the template for the translation of the mRNA message into a protein by the ribosome.

### Genomes: the basics  <a name="basics_genomes"></a>

A **genome** is an organism’s complete set of genetic material. Although every individual's genome is unique, the genomes of individuals of the same species will be very similar. It is useful to have a representative genome sequence for each species, and this is referred to as a reference genome. 

In the cell, genomes are organised into chromosomes. In practice, current DNA sequencing methods are unable to read the DNA sequence of a whole chromosome without errors. We therefore use the technique of sequencing shorter segments of chromosomes, and do it in such a way that the segments overlap and can be pieced together like a jigsaw puzzle. This process is referred to as genome assembly. For now, we will focus on what genome assemblies look like, and how they are represented in genome databases. 

The diagram below shows the structure of a typical assembly. It has 3 layers: the contigs are stretches of contiguous DNA sequence without gaps. The scaffolds are ordered sets of contigs separated by gaps of estimated length. In order to make scaffolds from contigs, techniques such as optical mapping and Hi-C are used. Finally, the chromosome is an ordered set of scaffolds separated by gaps on unknown length. To make the chromosome sequence from the scaffold, techniques such linkage mapping and FISH are used.

![](figures/figure_3.0.75.png)

Sometimes, there is insufficient (or no) data to reliably place a scaffold into a specific position on a chromosome. In the figure above, this is true of the scaffold on the right. The assembly above therefore comprises 2 toplevel sequences: 1 chromosome, and one unplaced scaffold.

### Sequence databases <a name="sequence_databases"></a>

Over the last few decades, as technology has evolved, we've seen an explosion in the number of genes and, later, genomes that have been sequenced. Sequence databases provide a place where these sequences can be deposited, stored and made available to the world. There are three widely-used nucleotide repositories (or primary databases) for the submission of nucleotide and genome sequences:

* [GenBank](https://www.ncbi.nlm.nih.gov/genbank), hosted by the National Center for Biotechnology Information (or NCBI).
* The [European Nucleotide Archive (ENA)](http://www.ebi.ac.uk/ena), hosted by the European Molecular Biology Laboratories (EMBL).
* The [DNA Data Bank of Japan (DDBJ)](http://www.ddbj.nig.ac.jp),  hosted by the National Centre for Genetics.

Together they form the [International Nucleotide Sequence Database Collaboration](http://www.insdc.org/about) and luckily for users, they all “mirror” each other. This means that irrespective of where a sequence is submitted, the entry will appear in all three databases. Once data are deposited in primary databases, they can be accessed freely by anyone around the world.

INSDC stores both primary data (i.e. the sequence reads exactly as they come off the machine) and assembled genomes (i.e. where an assembly algorithm has been used to build scaffolds or chromosomes from those reads). Commonly, these data are all stored together under what's known as a **BioProject**. Each BioProject is identified by an **accession**. Although every BioProject accession is a unique identifier for that project, they all start with a 5-letter code that denotes which INSDC database the data were submitted to: "PRJEB" for ENA, "PRJNA" for GenBank, and "PRJDB" for DDBJ. 

An AGP file is often also provided, describing how the contigs fit together as scaffolds, and how the scaffolds fit together as chromosomes. A genome project may also contain an annotation file in GFF format (more on this file format later). This file contains predicted gene structures: based on the genome sequence, certain algorithms can predict which regions encode genes. An example of a commonly-used gene prediction tools is [BRAKER](https://github.com/Gaius-Augustus/BRAKER). These predictions may or may not be guided by other types of evidence, such as RNA sequencing data. It is important to bear in mind that the majority of genes as they appear in the sequence databases (and also in WormBase ParaSite) are based on predictions: these predictions are driven by evidence, but most genes from helminth genome assemblies are unlikely to have been cloned and sequenced in their entirety. We'll look at an example of checking how well a gene model is supported by RNAseq evidence in the next WormBase ParaSite module.

**WormBase ParaSite takes sequence data from INSDC (a genome assembly and a set of gene predictions) and adds additional analyses that assist scientists in interpreting and querying this data. In this part of the module we will explore the basic functionality of the website for looking at helminth genes and genomes.**

---

# Practical Session I

In this practical session we will step into the shoes of real-world researchers trying to examine the genomic impact of mass drug administration of an anti-parasitic drug on *Schistosoma mansoni*. We will try to replicate parts of their methodology using WormBase ParaSite.

## The study

### Whole-genome sequencing of Schistosoma mansoni reveals extensive diversity with limited selection despite mass drug administration
#### Duncan J. Berger, Thomas Crellen, Poppy H. L. Lamberton, Fiona Allan, Alan Tracey, Jennifer D. Noonan, Narcis B. Kabatereine, Edridah M. Tukahebwa, Moses Adriko, Nancy Holroyd, Joanne P. Webster, Matthew Berriman & James A. Cotton

Control and elimination of the parasitic disease schistosomiasis relies on mass administration of praziquantel. Whilst these programmes reduce infection prevalence and intensity, their impact on parasite transmission and evolution is poorly understood. Here we examine the genomic impact of repeated mass drug administration on *Schistosoma mansoni* populations with documented reduced praziquantel efficacy. We sequenced whole-genomes of 198 *S. mansoni* larvae from 34 Ugandan children from regions with contrasting praziquantel exposure. Parasites infecting children from Lake Victoria, a transmission hotspot, form a diverse panmictic population. A single round of treatment did not reduce this diversity with no apparent population contraction caused by long-term praziquantel use. We find evidence of positive selection acting on members of gene families previously implicated in praziquantel action, but detect no high frequency functionally impactful variants. As efforts to eliminate schistosomiasis intensify, our study provides a foundation for genomic surveillance of this major human parasite.

---

In this paper, the researchers examine the genomic impact of repeated mass drug administration on *Schistosoma mansoni* populations with documented reduced praziquantel efficacy.

They collected samples from regions in Uganda with different exposure to praziquantel and performed whole genome sequencing to explore how schistosome populations change in response to repeated MDA as well as to monitor for the potential emergence and spread of praziquantel resistance.

![](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fs41467-021-24958-0/MediaObjects/41467_2021_24958_Fig1_HTML.png?as=webp)

Let's try to follow the same steps that these researchers used to perform their analysis using WormBase ParaSite.

## WormBase ParaSite Genome Browsing and Downloads

The researchers had to download The *S. mansoni* reference genome from WormBase Parasite to perform their genomic analyses.

### Task 1: Browse the genome list of WormBase ParaSite and S. mansoni genome statistics.

1. Go to WormBase ParaSite (https://parasite.wormbase.org/).
![](figures/home.png)

2. Click ”Genome List" at the top menu.<br>
This page lists all current genome assemblies in WormBase ParaSite. Information included about each are: data provider, assembly name, assembly id (linked to ENA), BioProject ID, clade and Genome Browser links.
![](figures/genome_list_pointer.png)
3. Use the Show/hide column at the top of the table to display more genome statistics for each genome.
![](figures/genome_list.png)
4. Click on Schistosoma mansoni to open its genome landing page.<br>
![](figures/genome_list_mansoni.png)

The genome page has useful summary information about the species and the assembly. You can see a summary of the methods used to produce the assembly and the annotation, and links to the publication describing it in more detail (where this is available).
![](figures/mansoni_genome.png)

6. Look now at the ‘Assembly statistics’ box.
The information in this box tells us about two metrics related to the quality of the assembly: contiguity and completeness.
![](figures/assembly_stats.png)<br>
**Contiguity**<br>
Contiguity describes how many scaffolds a genome is represented by: in a perfectly contiguous reference genome, the number of scaffolds would be equal to the number of chromosomes.<br><br>
Contiguity is described by several values, including the **total number of scaffolds in the assembly**, **the length of the longest scaffold**, the **N50 length** and the **N90 length**. If all of the scaffolds of the assembly were lined up in order of longest to shortest, the N50 length is the length of the shortest contig for which longer and equal length contigs cover at least 50 % of the assembly. <ins>For a given genome, a larger N50 length generally indicate a more contiguous assembly</ins>.<br><br>
**Completeness**<br>
BUSCO is a tool to assess completeness of genome assembly (BUSCO ASSEMBLY) and gene set (BUSCO ANNOTATION). It is based on the principle that some genes are so highly conserved across eukaryotic species that they should be present in any genome assembly, in single copy. <ins>Generally speaking, a higher percentage of single BUSCO genes, indicates a higher quality assembly</ins>. A word of warning though: BUSCO scores can be misleading for certain taxonomic groups. Although the genes are selected because they are supposed to be universally conserved, this is not always the case. Platyhelminth genomes tend to have lower BUSCO scores; this is not necessarily because the genomes are lower quality, but because some highly conserved eukaryotic genes are truly absent from this group of organisms.

Learn more about our widget [here](https://parasite.wormbase.org/info/Browsing/assembly_quality.html).

7. Mouse over the widget to explore the number of scaffolds of the S. mansoni genome. Note down the N50 length, and the BUSCO scores.<br><br>
You should see that:<br>- The assembly comprises of 12 scaffolds.<br>- The N50 length is 45.7 Mb and it's the length of the 4th scaffold.<br>- BUSCO annotation completeness is 81.6%.<br>- BUSCO assembly completeness is 72.9%.
![](figures/assembly_stats_n50.png)

8. Go back to the Genome List. Find out which *schistosoma* genome has the best BUSCO ANNOTATION score after *S. mansoni*.
You can hover your mouse over the pie chart in the BUSCO ANNOTATION or BUSCO ASSEMBLY pie chart to reveal the statistics. It looks like *S. japonicum* with PRJNA520774 BioProject ID has the best BUSCO scores after *S. mansoni*.
![](figures/japonicum_busco.png)

### Task 2: Download S. mansoni's reference genome from WormBase ParaSite.

Usually, many users, like our researchers, want to download the data for their genome-of-interest in various different formats, to perform their own analyses. WormBase ParaSite is a data hub and offers a number of compressed downloads for each species.

File formats available:

- FASTA: The FASTA format is a text-based format for representing either nucleotide sequences or amino acid (protein) sequences, in which nucleotides or amino acids are represented using single-letter codes. Read more [here](https://www.ncbi.nlm.nih.gov/genbank/fastaformat/).
- GFF: GFF is a standard file format for storing genomic features in a text file. GFF files are plain text, 9 column, tab-delimited files, frequently used for the representation of the gene features of a genome. Read more [here](https://www.ensembl.org/info/website/upload/gff3.html).
- GAF: GAFs are tab-delimited plain text files, where each line in the file represents a single association between a gene product and an ontology term (Gene Ontology, Phenotype, etc), with an evidence code, the reference to support the link between them, and other information.

You can download data from WormBase ParaSite using our Downloads page (https://parasite.wormbase.org/ftp.html)


1. Go to WormBase ParaSite (https://parasite.wormbase.org/)

2. Click "Downloads" at the top menu.

3. In the middle of the page you can find a table with genomes and their FTP links.
![](figures/downloads_main.png)

4. Search for "mansoni" in the filter text box at the top right corner of the table.

5. You can use the links appeared for *S. mansoni* to download the files you need. Which file would you download to perform whole genome sequencing alignment, as our researchers did?<br>Generally speaking, it's recommended to use unmasked reference genomes builds for alignment. That means, <ins>we should download and use the FASTA file linked under the "Genomic" column of the table.
![](figures/mansoni_download_fasta.png)
  
6. Click the FASTA button under the "Genomic" column for S. mansoni and a download will automatically start.

7. An alternative way to browse your downloads, is to directly browse our FTP server here: https://ftp.ebi.ac.uk/pub/databases/wormbase/parasite/releases/

## WormBase ParaSite: Gene pages
  
Researchers write: "The strongest signals of selection were detected within chromosome 2 regions ... Within one of these regions we identified a single locus (47.06–47.34 Mb) containing four sodium/potassium/calcium exchanger proteins (Smp_170450, Smp_336070, Smp_328710, Smp_094390) ... ".

After they discovered these important genes, researchers might want to investigate some basic information about their function, location, sequences etc. WormBase ParaSite's gene pages contain all these information that the researchers might find useful.

Through the following tasks, we're going to navigate to the gene page of one of the genes mentioned by the researchers (Smp_170450) and find information about the gene's function, transcripts, its UniProt ID, its genomic/protein sequences and more!

#### Task 3: Find general gene information (name, description, how many transcripts etc).

Our researchers would be interested in finding general information about the gene.

1. Go to WormBase ParaSite (https://parasite.wormbase.org/).

2. Paste the Gene ID (Smp_170450) in the search box at the top right corner of the page and press Enter.
![](figures/search_box.png)

3. The search will return the gene entry you searched for. Click on the Gene ID to open up the corresponding gene page.
![](figures/search_results.png)
  
4. You're on the gene page. Use the menu on your left to navigate.
![](figures/gene_page.png)  

You can learn more about the gene pages here (https://parasite.wormbase.org/info/Browsing/gene_pages.html).

#### Task 4: Use the “Region in detail” to visualise the gene in our genome browser. Do the same with Jbrowse.

It's quite useful for our researchers to visualise the gene model. This way they can learn more about gene's structure and gather information about the wider genomic regions (chromosomal position, nearby genes etc).
  
1. While on the gene page, click on the "Region in detail" button under the "Genomic context" header.
  
2. You can now browse the gene's location using the genomic browser. Use your mouse to navigate around the gene and hover over different features of the gene to see more information.<br>![](figures/region_in_details.png)<br> Here, each of the three boxes gives us an increasingly zoomed-in view of the gene’s genomic position. The top box shows the whole scaffold, and the middle box below it shows a zoomed-in part of the scaffold. The bottom box shows us the structure of the gene model.<br><br>We can see that:<br>(a) the gene is on the reverse strand - you can see this from the ‘<’ symbol located next to the gene name in the protein coding genes track.<br>(b) the gene has 9 exons in total. Both 5' and 3' UTRs (untranslated regions) are annotated.
  
4. You can use the "Configure tracks" button at the top left of the browser to load more tracks in the view.
  
5. You can use "Add RNAseq tracks" or "Add custom tracks".

6. You can learn more about the Genome Browser here (https://parasite.wormbase.org/info/Browsing/genome_browser_ensembl.html).
  
Using Jbrowse:

7. Click on the top-right "View region in Jbrowse" button to visualise the same region in a different genome browser called Jbrowse.
![](figures/open_jbrowse.png)    

8. You are being redirected to Jbrowse. When Jbrowse loads use your mouse to navigate around the gene and find nearby genes. Click on the gene models to see more information.
![](figures/jbrowse.png)      

9. Use the "Select tracks" at the top-left of the browser and select a few tracks to add to the view.

10. You can also load your own tracks by clicking "Track"->"Open track file or URL" from the top menu.

11. To learn more about Jbrowse visit our help page here (https://parasite.wormbase.org/info/Browsing/genome_browser_jbrowse.html).
  
Tip: Jbrowse is also accessible via a button in [WormBase ParaSite genome list](https://parasite.wormbase.org/species.html) and the [genome's landing page](https://parasite.wormbase.org/Schistosoma_mansoni_prjea36577).
 
12. Return back to the gene page for Smp_170450.

### Task 5: Find the genomic/protein sequence for this gene.

Researchers would also be interested in getting the different types of sequences that are available for the transcript of this gene.
  
**As well as gene pages, WormBase ParaSite has a page for each transcript that a gene produces. In this case, only one transcript isoform has been annotated.**

1. While on the gene page, click the transcript ID in the transcipt table to navigate to the transcript page.
![](figures/select_tr.png)
 
2. Click “Exons”, “cDNA” and “Protein” in the “Sequence” section of the navigation menu to see the different types of sequence that are available for the transcript.
![](figures/tr.png)

The “Exons” tab displays the sequence of individual exons in a table (useful if you’re interested in retrieving, say, only the sequence of exon 2); the “cDNA” tab has the cDNA sequence (the sequence you would get if you reverse transcribed mature mRNA); and the “Protein” tab has the amino acid sequence. All of the sequences can be downloaded in FASTA format. As well as the sequences displayed in the browser, you can also choose to download, for example, genomic sequence, just UTRs etc.
Exons sequences            | 
:-------------------------:|
![](figures/ex_seq.png)    |

cDNA sequence              | Protein sequence
:-------------------------:|:-------------------------:
![](figures/cDNA_seq.png)  | ![](figures/protein_seq.png)
4. Return back to the gene page for Smp_170450.

---
  
Ok! Now, our researchers have gathered general information about the genes they're interested in. They have also inspected their structure and sequence. However, they don't have any clues about the genes' function! What do these genes and their encoded proteins do?
  
Functional annotation tries to answer this question!<br>
![](https://ars.els-cdn.com/content/image/1-s2.0-S1570963914002799-fx1.jpg)

### Task 6: Functional annotation: Explore the Gene Ontology terms associated with this gene
A fast way to find out about the function of a gene’s product is to see which Gene Ontology (GO) terms have been associated with it.
  
Gene ontology is a formal representation of knowledge about a gene with respect to three aspects: Molecular Function, Cellular Component and Biological Process. Cellular Component GO terms describe where a protein is localised (in the membrane, extracellular, in the nucleus etc). Molecular Function GO terms describe the biochemical activity of the protein. Biological Process GO terms describe the pathways and broader processes that the protein contributes to.
 
1. Gene Ontology information is available at the gene page level. While on the gene page, click "Biological process" or "Cellular Component" or "Molecular Function" from the Gene ontology section of the navigation menu.
![](figures/click_go.png)
  
2. A table appears with information about the Gene Ontology terms that have been associated with this gene. You can click on the link under the "Accession" column to find more about each Gene Ontology term. 
![](figures/go_results.png)
  
According to these results, it looks like Smp_170450, that according to our researchers might play a role in PZQ resistance, is associated with transmembrane transport and calcium ion transport. Would this information be useful to our researchers? PZQ disrupts calcium ion homeostasis in the worm, so the fact that our gene is associated with calcium transport is a really important piece of information.

### Task 7: Functional annotation: Explore protein domains

Apart from Gene Ontology, the domains on the encoded protein might give us even more information about the function of the gene.
  
How we do go from a string of amino acids to predicting what this protein might do in the cell? This is where another type of database comes in: protein family databases. For the vast majority of predicted protein sequences, nobody will have done experiments to test what its function is. However, we can use the principle of homology to take proteins that are well-studied in one experimental system and infer that proteins of similar sequence in other organisms are likely to have similar structure, and therefore similar function. In reality, protein sequences are analysed in terms of domains: these are subsequences of a protein that have a defined tertiary structure or sequence motif, conferring a defined function. A protein can consist of several domains. When comparing proteins between organisms, often the region encoding a protein domain is highly conserved whilst the bit that connects different domains together is more divergent.

![](https://raw.githubusercontent.com/ProteinsWebTeam/interpro-docs/master/docs/images/member_databases/member_db.png)

A well known example of a protein domain database is Pfam. Pfam uses multiple sequence alignments of the known proteins with a certain domain to capture a representative model (a profile Hidden Markov Model) of that domain. Other protein domain databases, that might use slightly different methods to define domains, are: CATH, CDD, HAMAP, MobiDB Lite, Panther, PIRSF, PRINTS, Prosite, SFLD, SMART, SUPERFAMILY and TIGRfams. Luckily for us, all of these databases are united under the InterPro consortium.
 
1. Information about protein domains & features are available at the transcript page. To go to a transcript page you need to click on a transcript ID in the transcript table.
![](figures/select_tr.png)
  
2. On the left "Transcript-based displays" menu, click on "Domains & features".
![](figures/select_domain.png)

3. Use the tables to discover which domains and features have been annotated in this gene's protein.
![](figures/domains.png)  
  
According to the results, the domains in the encoded protein have to do with ion-binding and membrane exchange, agreeing with the Gene Ontology data for this gene.
  


---
  
Another approach to understanding what a gene does is comparing its sequence to other genes, both within the same genome, and across different genomes.
  
This analysis is called Comparative Genomics

### Task 8: Comparative Genomics: Find orthologues for your gene of interest in other species.

Wait! What orthologues and paralogues are? Read [here](https://sciencing.com/different-variants-gene-called-8092322.html) and/or [here](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2001-2-8-interactions1002) to find more!

<ins>In a nutshell</ins><br>
**Orthologues**: Genes which evolved from a common ancestral gene by speciation that usually have retained a similar function in different species.<br>
**Paralogues**: Paralogs are homologous genes that arise from gene duplication events. Their common ancestry and replicated sequence often leads to similar structure and function in related pathways and protein complexes.<br>

![](figures/Screenshot%202022-11-17%20at%2018.59.45.png)  
<ins>Why would researchers want to find orthologues in other species for their gene of interest?</ins> Function Annotation! If the function of this gene in S. mansoni is not known, you can check the function of its orthologues genes in other species like C. elegans or other Schistosomas. Many times you will find that orthologous genes function will be similar to this of your gene of interest.
  
1. While on the gene page, click "Orthologues" on the left "Gene-based displays" menu under "Comparative genomics".
![](figures/click_orth.png)

2. We need to wait a little bit for the orthologues to load.

3. When loaded, two tables are visible: "Summary of orthologues of this gene" and "Selected orthologues".
![](figures/orths.png)


4. On the left "Summary of orthologues of this gene" menu, you can select to display orthologues for one or more taxonomic groups (nematodes, platyhelminths)".
![](figures/orth_t1.png)
  
5. The second table shows the list of orthologues found for this gene.
![](figures/orth_t2.png)
  
6. You can use the search box at the top right to filter orthologues for *C. elegans* by typing "elegans". What is the function of this gene's orthologue in C. elegans? It looks like its a Na/Ca exchanger protein, further supporting our hypothesis!
  
7. Use the three buttons in the "Compare" column: "Alignment (protein)", "Alignment (cDNA)" and "Gene Tree (image)" to further explore the comparison.
![](figures/orth_t2_explore.png)

8. Click on the "Gene Tree (image)" of one of the orthologues in the list, to explore the gene tree for the specific orthologue.
![](figures/gene_tree.png)

9. You can follow the same instructions to discover paralogues too!

### Task 9: Functional Annotation: Explore phenotypes experimentally associated with this gene

Since release 16, WormBase ParaSite hosts 350,000 *C. elegans* and *S. mansoni* gene-phenotype associations. These associations have been curated from the literature over many years, from RNAi and variant data.

What about the other species? As the majority of helminth genes don’t currently have data from direct phenotypic assays, phenotypes have also been propagated between orthologues. For exaple, there are no gene-phenotype association data available for S. bovis. However, you can see the phenotypes associated with C. elegans or S. mansoni orthologues of your S. bovis gene of interest. Read more [here](https://wbparasite.wordpress.com/2021/09/06/announcing-wormbase-parasite-release-16/).

1. While on the gene page, click "Phenotypes" on the left "Gene-based displays" menu.
![](figures/clik_pheno.png)

2. We need to wait a little bit for the phenotypes to load.

3. When loaded, two tables are visible: "Phenotypes associated with this gene" and "Phenotype, disease and trait annotations associated orthologues of this gene in other species".
![](figures/phenos.png)

4. In the first "Phenotypes associated with this gene" table, you can find a list of phnoetypes, diseases and traits associated directly with this gene for this species, based on experimental evidence. If there are no associate phenotypes for your gene in the first table, a message showing "None Found" will be displayed. You can try and work with a different gene (i.e. Smp_025260) which has phenotype associations. Literature evidence for each association can be found under the "Study" column.
![](figures/ptab1.png)

5. The second table shows phenotype, disease and trait annotations associated orthologues of this gene in other species. Usually, there are not many phenotypic data available for parasitic worms, for this reason exploring phenotypes associated with other species like **C. elegans** is really useful for scientists. You can use the links in the table to navigate to the orthologous gene in the other species and find more information there.
![](figures/ptab2.png)

6. Gene-phenotype association links can also be found in our [Downloads FTP server](https://ftp.ebi.ac.uk/pub/databases/wormbase/parasite/releases/). Look for the files ending in ".phenotypes.gaf.gz"  and ".orthology-inferred_phenotypes.gaf.gz".

#### Task 10: Explore papers mentioning your gene of interest.

1. While on the gene page, click "Literature" on the left "Gene-based displays" menu.
![](figures/click_lit.png)

2. When loaded, a "Literature" table is visible. It lists the "Pubmed ID", "Title", "Authors" and "Journal" of all papers in EuropePMC about S. mansoni that mention your gene of interest.
![](figures/lit.png)

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

  
  
  
  4. On the left "Transcript-based displays" menu, click on the "AlphaFold predicted model"
  
5. Use the "AlphaFold predicted model" widget to discover the 3D protein structure of the protein
  
6. Use your mouse (drag/drop) to move and rotate the protein. You can zoom/unzoom using your mouse wheel
  
7. Use the right side menu to show/hide different protein/gene features (e.g. "Exons","PANTHER","Pfam" etc).

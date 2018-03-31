# awesome-alternative-splicing
## What is this?
This is a list of software packages (and the people developing these methods) for alternative splicing. [Contributions welcome](https://github.com/hussainather/awesome-alternative-splicing/blob/master/CONTRIBUTING.md)...

## Types of alternative splicing
 - Skipped exon or cassette exon (SE): An exon can be retained or spliced out of
 the primary transcript.
 - Mutually exclusion exons (MXE): One of two exons is retained in mRNA splicing
, but not both.
 - Alternative 5' splice site (A5SS): An alternative 5' splice junction (donor s
ite) is used that changes the 3' boundary of the upstream exon.
 - Alternative 3' splice site (A3SS): An alternative 3' splice junction (accepto
r site) is used that changes the 5' boundary of the downstream exon.
 - Retained intron (RI): A sequenced may be spliced out as an intron or retained
, and there are no flanking introns.

![Types of alternative splicing](images/altsplicetypes.jpeg) 

Source: http://rnaseq-mats.sourceforge.net/rmats3.0.9/

## Software packages
+ [flotilla](https://github.com/yeolab/flotilla) - [Python] - reproduce machine learning analysis of gene expression and alternative splicing data.
+ [GMAP](http://research-pub.gene.com/gmap/) - [C++] - detect complex variants and splicing in short reads, SNP-tolerant.
+ [HMMSplicer](http://derisilab.ucsf.edu/index.php?software=105) - [C++] discovery canonical and non-canonical splice junctions in short read datasets.
+ [MapSplice](http://www.netlab.uky.edu/p/bioinfo/MapSplice2) - [C++] - map RNA-seq data to reference genome for splice junction discovery.
+ [MISO](http://genes.mit.edu/burgelab/miso/) - determine alternative splicing expression. 
+ [outrigger](https://github.com/YeoLab/outrigger) - [Python] - calculate alternative splicing scores of RNA-Seq data based on junction reads and a de novo, custom annotation created with a graph database, especially made for single-cell analyses.
+ [rMATS](http://rnaseq-mats.sourceforge.net/) - [Python] - RNA-Seq Multavariate Analysis of Transcript Splicing. [Reading rMATS output](https://www.biostars.org/p/256949/)
+ [rmats2sashimiplot](https://github.com/Xinglab/rmats2sashimiplot/) - [Python] - visualize rMATS output using sashimi plots.
+ [SingleSplice](https://github.com/jw156605/SingleSplice) - [R, perl, C++] - detect biological variation in alternative splicing within a population of single cells. 
+ [SpliceMap](https://web.stanford.edu/group/wonglab/SpliceMap/) - [C++] - discover and align splice junctions for RNA-Seq reads.
+ [SpliceR](http://www.bioconductor.org/packages/2.13/bioc/html/spliceR.html) - detect alternative splicing and predict coding potential. 
+ [SplicingCompass](https://www.leibniz-hki.de/en/SplicingCompass.html) - detect differential splicing using RNA-Seq data.
+ [STAR](https://code.google.com/archive/p/rna-star/) - identify alternative splicing.
+ [TopHat](http://ccb.jhu.edu/software/tophat/index.shtml) [C++] - map splice junctions for RNA-Seq reads.


## Review of RNA-Seq splicing tools
**Tool**|**Performs split-read alignment**|**Transcript reconstruction (assembly)**|**Expression Analysis (any)**|**Gene expression analysis**|**Transcript specific expression analysis**|**Exon junction expression**|**Quantitative alternative expression analysis**|**Expression level sensitivity**|**Output**|**Minimum read length required or recommended**|**Visualization tool**|**Performs comparisons between conditions (ex. tumor vs normal)**|**Relevant comparison to Alexa-seq**|**Data type supported**|**Citation**| | | | | | | | | | | 
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
Alexa-Seq|N|N|Y|Y|Y|Y|Y|Junction|"Expression and structure information for junctions and genes; UCSC track info| extensive alternative expression visualization / statistics / graphs"|No minimum (tested on 36bp-100bp reads)|"Extensive| includes custom graphs and links to UCSC browser"|Y|-|Illumina|In preparation| | | | | | | | | 
Cufflinks|N|Y|Y|Y|Y|N|Y|Transcript|"Transcript information and expression statistics| BED| GTF"|75bp|UCSC browser|Y|Y|Paired-end Illumina reads|"Trapnell et al.| 2010| Nat. Biotech.| 28:511-515"| | | | | | 
Scripture|N|Y|Y|N|N*|N|N|Transcript*|"Transcript structure information and non-parsimonious expression statistics| BED"|75bp|UCSC browser|N|N|Illumina|"Guttman et al.| 2010| Nature Biotech| 28:503-510 | http://www.nature.com/nbt/journal/v28/n5/abs/nbt.1633.html"| | | | | | | 
SpliceMap|N|N|Y|Y|N|Y|N|Junction|"Alignments. SAM| BED| Wig"|50bp|UCSC browser|N|N|Illumina|"Au et al.| 2010| NAR| DOI 10.1093/nar/gkq211 | http://www.stanford.edu/group/wonglab/SpliceMap/SpliceMap.pdf"| | | | | | 
TopHat|Y|N|N|N|N|Y|N|Junction|"Alignments. SAM| BED| Wig"|75bp|N|N|N|Illumina|"Trapnell C| Pachter L| Salzberg SL. 2009| Bioinformatics| 25(9):1105-1111 | Langmead et al.| 2009| Genome Biol.| 10(3):R25"| | 
MMES|Y|N|N|N|N|Y|N|Junction|Identified splice junctions and p-values|25bp|N|N|N|Illumina|"Wang et al.| Plos One| 2010| Vol 5| Iss 1| e8529"| | | | | | 
G-Mo.R-Se|Y|Y|N|N|N|N|N|Transcript*|Transcript structure information.  GFF|25bp|Grape Genome Browser|N|N|Illumina|"Denoeud et al.| 2008| Genome Biol| 9(12):R175 | http://genomebiology.com.ezproxy.library.ubc.ca/content/pdf/gb-2008-9-12-r175.pdf"| | | | | | | | 
SplitSeek|Y|N|N|N|N|Y|N|Junction|Alignments.  BED|50bp|UCSC browser|N|N|SOLiD only|"Ameur et al.2010| Genome Biol.| 11(3):R34. | http://genomebiology.com/content/pdf/gb-2010-11-3-r34.pdf"| | | | | | | | | 
GSNAP|Y|Y|N|N|N|N|N|N/A|Alignments.  SAM and FASTA|Minimum 14bp (tested on 36bp reads)|UCSC browser|N|N|Illumina | sodium bisulfite-treated DNA sequencing (for analysis of methylation status)|"Wu and Nacu| 2010| Bioinformatics| 26(7):873-881 | http://bioinformatics.oxfordjournals.org/cgi/content/full/26/7/873"| | | | | | | | 
 | | | | | | | | | | | | | | | | | | | | | | | | | | 
* Transcript expression values are non-parsimonious| | | | | | | | | | | | | | | | | | | | | | | | | | 
** Not supported (current version not stable)| | | | | | | | | | | | | | | | | | | | | | | | | | 
 | | | | | | | | | | | | | | | | | | | | | | | | | | 
 | | | | | | | | | | | | | | | | | | | | | | | | | | 
Tool|Performs split-read alignment|Transcript reconstruction (assembly)|Expression Analysis (any)|Gene expression analysis|Transcript specific expression analysis|Exon or Junction expression|Quantitative alternative expression analysis|Expression level sensitivity|Output|Minimum read length required or recommended|Ability to identify rearrangements / indels|Junction Identification|Implementation|Public tool|Open Source|Validated events|Validation method|Visualization tool|Performs comparisons between conditions (ex. tumor vs normal)|Relevant comparison to Alexa-seq|Practical comparison to Alexa-seq|Organism and Tissue Samples (for publicly available analyses to date)|Data type supported|Citation|URL| 
Alexa-seq|N|N|Y|Y|Y|Y|Y|Junction|"Expression and structure information for junctions and genes; UCSC track info| extensive alternative expression visualization / statistics / graphs"|No minimum (tested on 36bp-100bp reads)|N|Database|Perl/R/Unix|Y|Y (GPL)|88% of 192 alternatively expressed exon by qPCR | 85% of 189 alternatively expressed exon junctions by RT-PCR and 61 of these were verified by Sanger sequencing | Additional comparisons to mRNA/EST sequence databases and matched splicing microarray data|"RT-PCR| qPCR| Sanger Sequencing| mRNA/EST alignments| Splicing microarrays"|"Extensive| includes custom graphs and links to UCSC browser"|Y|-
Cufflinks|N|Y|Y|Y|Y|N|Y|Transcript|"Transcript information and expression statistics| BED| GTF"|75bp|N|Predicted from data|C++|Y|Y|5/5 alternatively spliced genes by RT-PCR | 51% of novel isoforms and 62% of novel isoforms observed in multiple timepoints validated by ESTs and RefSeqs | 153/185 novel TSS validated using ChIP-seq peaks|RT-PCR | EST and RefSeq alignments | ChIP-seq|UCSC browser|Y|Y|Y|Mouse myoblast cell line at multiple differentiation timepoints|Paired-end Illumina reads|"Trapnell et al.
Scripture|N|Y|Y|N|N*|N|N|Transcript*|"Transcript structure information and non-parsimonious expression statistics| BED"|75bp|N|Predicted from data|Java|Y|Unknown|90% of downstream alternative 5′ start sites and 75% of upstream alternative 5′ start sites contained an H3K4me3 modification | Novel 3' exons supported by poloyadenylation motifs in 60% of 551 cases | 83% of 588 novel internal exons maintained ORF and were highly conserved  | 5/5 novel exons validated using RT-PCR and Sanger sequencing|H3K4me3 marks on alternative promoters | polyadenylation motifs supporting alternate 3' ends | RT-PCR of novel exons followed by Sanger sequencing|UCSC browser|N|N|N|"Mouse ESCs| NPCs| ATCCs"|Illumina
SpliceMap|N|N|Y|Y|N|Y|N|Junction|"Alignments. SAM| BED| Wig"|50bp|N|Predicted from data|Python|Y|Unknown|"87.9% of all (151|317) junctions| and 41.2% of all novel (23|020) junctions were supported by at least one EST | 17 (85%) of 20 novel junctions validated by RT-PCR; 13 (92.9%) of 14 novel junctions with multiple-read support validated by RT-PCR"|EST mapping | RT-PCR|UCSC browser|N|N|N
TopHat|Y|N|N|N|N|Y|N|Junction|"Alignments. SAM| BED| Wig"|75bp|N|Predicted from data|C++/Python|Y|Unknown|None|N/A|N|N|N|N|Mouse brain|Illumina|"Trapnell C
MMES|Y|N|N|N|N|Y|N|Junction|Identified splice junctions and p-values|25bp|N|Predicted from data|Published algorithm only|N|N/A|"20/20 false positives (FP) validates| and 30% of undisclosed number of false negatives (FN)"|"RT-PCR for FP| EST support for FN"|N|N|N|N|"Mouse brain| liver| muscle;  Human embryonic kidney and B-cell lines"
G-Mo.R-Se|Y|Y|N|N|N|N|N|Transcript*|Transcript structure information.  GFF|25bp|N|Predicted from data|Perl|Y**|Y|"175 (18.5%) of 944 cDNA non-intron-retention events were also found by G-Mo-R-Se | including: 7.2% of skipped exons| 25% of mutually exclusive exons| 22.6% of alternative donor/acceptor sites (note: method is not able to find intron retention events)"|"comparison to cDNA library from same tissues: 944 events detected in cDNA librarys vs 1|602 events detected by G-Mo-R-Se = 175 events in common."|Grape Genome Browser|N|N|N|"Grape leaf
SplitSeek|Y|N|N|N|N|Y|N|Junction|Alignments.  BED|50bp|Y|Predicted from data|Perl|Y|Y (GPL)|2 exon junctions in 2 genes|EST and gene prediction support|UCSC browser|N|N|N|Mouse oocytes (2)|SOLiD only|"Ameur et al.2010| Genome Biol.| 11(3):R34. | http://genomebiology.com/content/pdf/gb-2010-11-3-r34.pdf"
GSNAP|Y|Y|N|N|N|N|N|N/A|Alignments.  SAM and FASTA|Minimum 14bp (tested on 36bp reads)|Y|Database or predicted form data|"Source code in C| utility programs in Perl"|Y|Unknown|None|N/A|UCSC browser|N|N|N|"Human UHR from MAQC| simulated reads from genome with introduced mutations and indels"|Illumina | sodium bisulfite-treated DNA sequencing (for analysis of methylation status)|"Wu and Nacu
 | | | | | | | | | | | | | | | | | | | | | | | | | | 
* Transcript expression values are non-parsimonious| | | | | | | | | | | | | | | | | | | | | | | | | | 
** Not supported (current version not stable)| | | | | | | | | | | | | | | | | | | | | | | | | | 

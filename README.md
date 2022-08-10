## Characterising-the-naked-mole-rat-microbiota-an-exploratory

After decades of research on model animals chosen due to convenience and similarity to humans, interest has recently expanded to include species exhibiting unusual features. One such animal is the naked mole-rat (NMR), a rodent that is, among other features resistant to ageing and the development of cancer. A substantial role in these fascinating properties may be mediated by the gastrointestinal (GI) microbiome. The microbiome can be understood as a complex biotope in continuous interaction with its host. It is optimally adapted to its environment, just one example is the adaptation to the changing microenvironment along the GI tract. For a holistic characterisation of the gut microbiome, it is therefore important to consider possible differences in microbial composition and function along the GI tract.
To reveal distinguishing features of the NMR microbiome and help explain their unique properties, a section-based bioinformatical analysis of metagenomic data was conducted. Taxonomic and KEGG orthology abundance tables were derived from shotgun metagenomic sequencing data from gut sections of three NMRs (caecum, colon, and stool) and 16 mice (duodenum, jejunum, ileum, caecum, colon, and stool), and resulting taxonomic and functional profiles were analysed using RStudio.
	The analysis revealed a consistent taxonomic profile in NMR caecum, colon, and stool, while significant differences were seen in function between caecum and stool. In mice, differences were seen between small and large intestines on taxonomic and functional levels. Microbiome composition and functional profiles were significantly different between the two models, although a large overlap in functional pathway was observed. Investigation of features seen in NMR but not mouse samples revealed characteristics potentially unique to the NMR, such as the novel discovery of Odoribacteraceae and microbial biosynthesis of bile-acids and steroid hormones. 
	Although the results must be validated in larger cohorts, our findings represent the first description of microbial and functional features in the GI tract of NMRs
  
  # Dataset
DNA extraction was conducted under a hood with laminar flow (LabGarda ES Energy Sever Classe II Laminar Flow, NuAire Inc., Plymouth, MN, USA) to limit environmental contamination. Total DNA was extracted from all samples with the ZymoBIOMICS DNA Miniprep Kit (ZYMO Research Europe GmbH, Freiburg, Germany) following the manufacturers’ protocol. The extracted DNA was stored at -20°C until shipment to Novogene on dry ice for whole genome shotgun sequencing.

Raw data were processed using the NGLess39 v1.3.0 pipeline. Quality trimming was performed by discarding base calls with Phred scores below 25, corresponding to a base call accuracy of 99.7%, as well as discarding any reads shorter than 45 bp after trimming. To avoid contamination with host DNA or lab contamination, the quality-controlled reads were filtered for host and human reads. NMR reads were mapped to the host genome Heterocephalus glaber (GCA_000247695.1 HetGla_female_1.0, NCBI), and Homo sapiens (GCF_000001405.39 GRCh38, NCBI) genomes using bbtools.40 Mouse reads were mapped to the Mus musculus genome (GCA_000001635.8 GRCm38.p6, NCBI). All reference genomes were masked using the ProGenomes2 database.41 The reads which passed quality control were mapped to the masked NMR and mouse reference using bwa within the NGLess pipeline. Sequences matching the references were considered off-targets and discarded. 

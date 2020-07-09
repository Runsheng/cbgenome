# cbgenome
**The C. briggsae genome and annotation files.**



## cbont genome

The genome assembly build from de novo assembly of Nanopore long reads.

file list: 

- cbont_genome.fa: the genome in chromosome level (no gap remains, including mtDNA). 
- cbont_genome.gff: the gene prediction results in gff3 format
- cbont_mrna-transcripts.fa: the mRNA sequence file 
- cbont_cds-transcripts.fa: the CDS sequence file
- cbont_proteins.fa: the protein sequence file
- cbont.agp: the agp file used to build the genome from  scaffolds (contig) using Hi-C linkage
- cbont.chain: the chain file to liftover the annotation between scaffold and chromosome-level genome
- scaffold.tar: the genome files in scaffold level
  - cbont_scaffolds.fa: the scaffold sequence file
  - cbont_scaffold.gff: the annotation for scaffold level



## cb4i genome

The genome assembly originated from cb4 contigs. The contig orders were adjusted by Hi-C linkage. 

File location: ./cb4i

- cb4i.fasta: the genome sequence file 
- cb4i.gff: the liftover gff annotation from WormBase WS260 cb4 annotation
- ./agp/: agp files to build the cb4i from cb4 genome
  - cb4_split1.agp
  - cb4_split2.agp
  - cb4i_build.agp
- ./chain/: chain files:
  - cb4_split1.chain
  - cb4_split2.chain
  - cb4i_build.chain
- ./liftover/: the missing part in gff annotation when doing liftover
  - 1.gff.unmap: the unmapped part of the cb4 gff when using cb4_split1.chain
  - 2.gff.unmap: the unmapped part of the cb4 gff when using cb4_split2.chain
  - cb4i.gff.unmap: no unmapped part

Known issues:

- Missing genes from cb4_annotation because of the liftover (339 protein-coding in total). 
- Some chromosome start and/or end with "N" to indicate the ends are newly formed


# cbgenome
**The C. briggsae genome and annotation files.**



## cb4i genome

The genome assembly originated from cb4 contigs. The contig order was adjusted by 

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

Known issues:

- Missing genes from cb4_annotation because of the liftover (339 protein-coding in total). 
- Some chromosome start and/or end with "N" to indicate the ends are newly formed



## cbont genome

The genome assembly build from de novo assembly of Nanopore long reads.

file location: ./cbont: the genome file in chromosomes level

- cbont.fasta: the genome 
- cbont.gff: the prediction result from 



./scaffold/: the genome files in scaffold level

- cbont_scaf.fasta: the polished scaffold used to build the final genome.
- cb4ont.agp: the agp file indicate the scaffold to chromosome build indicated by Hi-C linkage. 


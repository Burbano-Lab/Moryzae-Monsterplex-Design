# Moryzae-Monsterplex-Design

This Monsterplex version for Magnaporthe oryzae samples aims to distinguish the isolates in various levels:
* Host specificity classification
* Clonal lineage classification
* Mating type classification
* Presence and absence of effector genes and their allele type

## Host specificity classification

We have used three major criteria to select the SNPs:
* The SNP must be fixed in the target population
* The SNP should maximise the distance between the target population and the rest, e.g. SNPs in which their Fst value is ~1 between the target population and individuals distinct from that same population.
* Only a 10% of missing information was allowed in the target popualtion

We generated a repertoire of 63,122 candidate SNPs distributed as following:

Host     | Number of Disgnostic SNPs
-------- | --------------
Eleusine | 1,344
Lolium   | 623
Oryza    | 141
Setaria  | 605
Triticum | 500
Zea      | 9,073

[The repertoire of the candidate SNPs can be found here](/data/multiple_hosts.SNPs.FstFiltered.tsv)

We centered the SNPs inside windows of 200 bps as in the following example:

```bash
>Eleusine-A-Contig01-193667-AG006
[...100-bases...CGCGGGAATT...N...CCAAATACCC...100-bases]
                             |
   		   Position of the SNP
```
In this example, this window contains a SNP diagnostic for the ***Triticum*** lineage. The diagnostic SNP is "A"
The positional information (Contig01:42936) as well as the assembly used as reference (AG006) is shown in the header.

[The file containing the windows in fasta format can be found here](/data/multiple_hosts.SNPs.FstFiltered.fasta)


## Clonal lineages classification
Similarly, here we provide the files for the identification of the following *M. oryzae* clonal lineages:

Host    | Clonal lineage | Numer of Diagnostic SNPs
------- | -------------- | -------------
Tritcum | B71            | 2,392 
Oryza   | II             | 3,008
Oryza   | III            | 2,815
Oryza   | IV             | 2,731

[The repertoire file can be found here](/data/clonal_lineages.SNPs.tsv)
[The file containing the windows in fasta format can be found here](/data/clonal_lineages.SNPs.fasta)

# Adapter Finder
## What is a sequence adapter?
Sequence adapters are short DNA sequences serving the scope of fishing a (generally
unknown) DNA sequence of interest for various purposes. Next Generation Sequencers (NGS) employ adapters
to immobilize DNA fragments to sequencer flow cells in order to initiate bridge
amplification as well as for downstream assignment of reads to the right samples. They are
typically ligated to every single DNA molecule during library preparation.


Workflows that process NGS data typically include a step to filter or remove (trim) adapter
sequences. 

Here we will design a tool to determine if adapter sequences have been trimmed properly
in an input FASTQ file. As a first step to solve this problem, we must calculate and
output the frequency of all k-mers found in the input sequencing data, given an
adapter of length k. Our tool will take two inputs: a FASTQ genomic data file and the adapter length (k) and will output a sorted list of all k-mers identified along with their frequency as observed in the input data:

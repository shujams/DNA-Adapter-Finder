# Adapter Finder
![image text](https://www.thoughtco.com/thmb/gOEbyq2I6Wwh3CB1KR1_5zCr-9k=/768x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/3-D_DNA-56a09ae45f9b58eba4b20266.jpg)
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
adapter of length k. This tool determines if adapter sequences have been trimmed properly in an input FASTQ file and will sort adapters based on k-mer length. Furthermore, it can find specific (including potential overlapping) user defined DNA adapter sequences and return their counts.

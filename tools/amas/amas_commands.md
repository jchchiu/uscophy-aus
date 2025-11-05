## Example of code to run AMAS
```
( AMAS.py concat \
  -f fasta \
  -d aa \
  --concat-out {output.matrix} \
  --concat-part {output.partitions} \
  --part-format nexus \
  -i {input}  )
  ```

## Required arguments
```
required arguments:
  -i IN_FILES [IN_FILES ...], --in-files IN_FILES [IN_FILES ...]
                        Alignment files to be taken as input. You can specify multiple files using
                        wildcards (e.g. --in-files *fasta)
  -f {fasta,phylip,nexus,phylip-int,nexus-int}, --in-format {fasta,phylip,nexus,phylip-int,nexus-int}
                        The format of input alignment
  -d {aa,dna}, --data-type {aa,dna}
                        Type of data
```			

## Action arguments
### Concatenate input alignments (concat)
```
options:
  -h, --help            show this help message and exit
  -p CONCAT_PART, --concat-part CONCAT_PART
                        File name for the concatenated alignment partitions. Default: 'partitions.txt'
  -t CONCAT_OUT, --concat-out CONCAT_OUT
                        File name for the concatenated alignment. Default: 'concatenated.out'
  -u {fasta,phylip,nexus,phylip-int,nexus-int}, --out-format {fasta,phylip,nexus,phylip-int,nexus-int}
                        File format for the output alignment. Default: fasta
  -y {nexus,raxml,unspecified}, --part-format {nexus,raxml,unspecified}
                        Format of the partitions file. Default: 'unspecified'
  -e, --check-align     Check if input sequences are aligned. Default: no check
  -c CORES, --cores CORES
                        Number of cores used. Default: 1
```

### Convert to other file format (convert)
```
options:
  -h, --help            show this help message and exit
  -u {fasta,phylip,nexus,phylip-int,nexus-int}, --out-format {fasta,phylip,nexus,phylip-int,nexus-int}
                        File format for the output alignment. Default: fasta
  -e, --check-align     Check if input sequences are aligned. Default: no check
  -c CORES, --cores CORES
                        Number of cores used. Default: 1
```		

### Create replicate datasets for phylogenetic jackknife (replicate) 	
```
options:
  -h, --help            show this help message and exit
  -r REPLICATE_ARGS REPLICATE_ARGS, --rep-aln REPLICATE_ARGS REPLICATE_ARGS
                        Create replicate data sets for phylogenetic jackknife [replicates, no
                        alignments for each replicate]
  -u {fasta,phylip,nexus,phylip-int,nexus-int}, --out-format {fasta,phylip,nexus,phylip-int,nexus-int}
                        File format for the output alignment. Default: fasta
  -e, --check-align     Check if input sequences are aligned. Default: no check
  -c CORES, --cores CORES
                        Number of cores used. Default: 1
```

### Split alignment according to a partitions file (split)
```
options:
  -h, --help            show this help message and exit
  -l SPLIT_BY, --split-by SPLIT_BY
                        File name for partitions to be used for alignment splitting.
  -j, --remove-empty    Remove taxa with sequences composed of only undetermined characters? Default:
                        Don't remove
  -u {fasta,phylip,nexus,phylip-int,nexus-int}, --out-format {fasta,phylip,nexus,phylip-int,nexus-int}
                        File format for the output alignment. Default: fasta
  -e, --check-align     Check if input sequences are aligned. Default: no check
  -c CORES, --cores CORES
                        Number of cores used. Default: 1
```

### Write alignment summary (summary)
```
options:
  -h, --help            show this help message and exit
  -o SUMMARY_OUT, --summary-out SUMMARY_OUT
                        File name for the alignment summary. Default: 'summary.txt'
  -s, --by-taxon        In addition to alignment summary, write by sequence/taxon summaries. Default:
                        Don't write
  -e, --check-align     Check if input sequences are aligned. Default: no check
  -c CORES, --cores CORES
                        Number of cores used. Default: 1
```

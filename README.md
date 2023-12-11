A simple script to run prodigal on a genome FASTA file, using code/thresholds from GTDB-tk to decide on various parameters for prodigal. Prodigal is run twice, once using translation table 4 and once with 11, and the gene predictions for one of these options is chosen. 

The only dependency is the [SingleM](wwood.github.io/SingleM/) package, since further dependencies such as `prodigal` are included underneath. To use:

```
mamba create -n singlem -c conda-forge -c bioconda singlem
mamba activate singlem
./bin/prodigal-runner run -h
./bin/prodigal-runner run -i /path/to/genome.fasta -o /path/to/output_directory -t NUM_THREADS
```

## Citation
Since this is just a wrapper around GTDB-tk, please cite the GTDB-tk paper if you use this script:

Chaumeil, Pierre-Alain, Aaron J. Mussig, Philip Hugenholtz, and Donovan H. Parks. "GTDB-Tk v2: memory friendly classification with the genome taxonomy database." Bioinformatics 38, no. 23 (2022): 5315-5316.

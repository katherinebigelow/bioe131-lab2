# Lab 2 Writeup
## commands:

```
muscle -in seqs.fa -out seqs.aligned.fa

MUSCLE v3.8.31 by Robert C. Edgar

http://www.drive5.com/muscle
This software is donated to the public domain.
Please cite: Edgar, R.C. Nucleic Acids Res 32(5), 1792-97.

seqs 48 seqs, max length 2217, avg  length 2209
00:00:00      6 MB(0%)  Iter   1  100.00%  K-mer dist pass 1
00:00:00      6 MB(0%)  Iter   1  100.00%  K-mer dist pass 2
00:00:06     79 MB(4%)  Iter   1  100.00%  Align node
00:00:06     79 MB(4%)  Iter   1  100.00%  Root alignment
00:00:09     79 MB(4%)  Iter   2  100.00%  Refine tree
00:00:09     79 MB(4%)  Iter   2  100.00%  Root alignment
00:00:09     79 MB(4%)  Iter   2  100.00%  Root alignment
00:00:21     79 MB(4%)  Iter   3  100.00%  Refine biparts
00:00:34     79 MB(4%)  Iter   4  100.00%  Refine biparts
00:00:34     79 MB(4%)  Iter   5  100.00%  Refine biparts
00:00:34     79 MB(4%)  Iter   5  100.00%  Refine biparts
```

The input is the sequences, and the output is placed in seqs.aligned.fa, which is essentially the input sequences but with (---) to align them, as well as what's probably how close they are to each other.

```
fasttree -nt < seqs.aligned.fa > tree.nwk
FastTree Version 2.1.10 No SSE3
Alignment: standard input
Nucleotide distances: Jukes-Cantor Joins: balanced Support: SH-like 1000
Search: Normal +NNI +SPR (2 rounds range 10) +ML-NNI opt-each=1
TopHits: 1.00*sqrtN close=default refresh=0.80
ML Model: Jukes-Cantor, CAT approximation with 20 rate categories
Initial topology in 0.08 seconds
Refining topology: 22 rounds ME-NNIs, 2 rounds ME-SPRs, 11 rounds ML-NNIs
Total branch-length 0.954 after 0.76 sec2, 1 of 46 splits
ML-NNI round 1: LogLk = -15621.453 NNIs 8 max delta 16.59 Time 1.13
Switched to using 20 rate categories (CAT approximation)1 of 20
Rate categories were divided by 0.740 so that average rate = 1.0
CAT-based log-likelihoods may not be comparable across runs
Use -gamma for approximate but comparable Gamma(20) log-likelihoods
ML-NNI round 2: LogLk = -14251.186 NNIs 2 max delta 0.00 Time 1.37
Turning off heuristics for final round of ML NNIs (converged)
ML-NNI round 3: LogLk = -14251.086 NNIs 0 max delta 0.00 Time 1.64 (final)
Optimize all lengths: LogLk = -14251.086 Time 1.72
Total time: 2.18 seconds Unique: 48/48 Bad splits: 0/45
```

After seeing the tree drawn out in the .ipynb, hu and bb seem related (as well as cy and rh), with pi distantly related.

The specimens I picked and their results from BLAST were:

pi.3: "adeno-associated virus isolate pi.3 capsid protein VP1 (cap)gene"

hu.66: "adeno-associated virus isolate hu.66 capsid protein VP1 (cap) gene"

cy.6: "non-human primate adeno-associated virus isolate AAVcy.6 capsid protein (VP1) gene"

rh.51 "adeno-associated virus isolate rh.51 capsid protein VP1 (cap) gene"

rh.52 "adeno-associated virus isolate rh.52 capsid protein VP1 (cap) gene"

The specimens I picked all seem to be somewhat related in that they all code for capsid proteins.

We might not trust the annotations for sequences as they may have been inputted under incorrect assumptions.

For the AT vs GC content of each cluster, as I only picked clusters as closely related to each other, the AT/GC content is very heavily skewed towards each end. In addition, they all have around the same sequence length.





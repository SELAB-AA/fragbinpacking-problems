[![DOI](https://zenodo.org/badge/60609393.svg)](https://zenodo.org/badge/latestdoi/60609393)
# fragbinpacking-problems
Problem Sets for the Fragmentable Items Bin Packing Problem

Each problem instance has the lowest number of bins possible.
That is, bin_count = ceil(sum(items) / bin_capacity).

optimal_block_counts.txt contains the optimal number of blocks,
which is related to the optimal number of fragments as
bin_count + item_count + slack - block_count,
excluding those eliminated by algorithms E1 and E2.

Its format is lines identifying problem classes:
{bin_capacity, item size lower bound, item size upper bound, item_count}
followed by the optimal block counts for each of the 10 problems in order of appearance.

The problem instances of each problem class is contained in a gzip compressed file named
uniform_{capacity}_{low}_{high}_{items}.gz, where {capacity} is the bin capacity,
{low} and {high} are the range of item sizes and {items} is the number of items.

The format of the problem instance files is 5 comment lines, repeating the information
contained in the file name, followed by lists of space-separated item sizes, one line per problem instance.


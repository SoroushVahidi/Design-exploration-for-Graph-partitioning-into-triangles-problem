# Partition Into Triangles: Three Exact Approaches (C++)

> Historical undergraduate project (2020), kept for reference.

**What this is.** **Partition Into Triangles** asks whether the vertices of a graph can be split into disjoint triangles (3-cliques). It is NP-complete even on graphs of bounded degree. This project implements and compares three exact approaches in C++. One follows the algorithm of van Rooij, van Kooten Niekerk and Bodlaender for bounded-degree graphs, one is an inclusion–exclusion style counting method, and one is my own backtracking design.

## References

- J. M. M. van Rooij, M. E. van Kooten Niekerk, H. L. Bodlaender. *Partition Into Triangles on Bounded Degree Graphs.* Theory of Computing Systems, 2013. [doi:10.1007/s00224-012-9412-5](https://doi.org/10.1007/s00224-012-9412-5)
- My literature review of this problem (in Persian): S. Vahidi, *Literature review about the problem "partition graph into triangles"*, 2020. DOI: [10.13140/RG.2.2.13359.36006](https://doi.org/10.13140/RG.2.2.13359.36006)

## Files

| File | What it is |
|---|---|
| `rooij approach.cpp` | Implementation following van Rooij et al. Also reads `satout.txt`, the output of an external SAT solver run |
| `ie approach.cpp` | Inclusion–exclusion / counting approach (uses binomial coefficients). Reads `o7.txt` |
| `my approach.cpp` | My own search-based approach with a triangle check (`is_triangle`) |
| `گزارش.pdf` | Project report in Persian ("گزارش" means "report") |

## Build

Each file is a standalone program:

```bash
g++ -O2 -o rooij "rooij approach.cpp"
g++ -O2 -o ie "ie approach.cpp"
g++ -O2 -o mine "my approach.cpp"
```

Input graph files are opened by name inside each program (for example `o7.txt`). Test instances are not included.

## License

MIT, see `LICENSE`. The algorithm in `rooij approach.cpp` is due to the authors cited above.

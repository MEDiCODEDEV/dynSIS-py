# Optimized Gillespie algorithms for the efficient simulation of Markovian epidemic processes on large and heterogeneous networks: SIS-OGA

### Python implementation

## Versions

[Fortran implementation - for performance](https://github.com/wcota/dynSIS)

[(this) Python implementation - learn and use](https://github.com/wcota/dynSIS-py)

[NetworkX Python implementation - range of options](https://github.com/wcota/dynSIS-networkx)

## Synopsis

This code is a implementation of the SIS-OGA algorithm, as detailed in our paper (to be cited). It receives as input a network file, containing a list of edges and read, via terminal, the dynamical parameters.

For performance, see https://github.com/wcota/dynSIS (Fortran implementation)

## Dataset input

You need to provide a file containing the list of edges (__in__ and __out__, two collumns). ID of the vertices must be enumerated sequentially as `1, 2, 3,..., N`, where `N` is the total number of vertices of the network. Here, we assume  __undirected__ and __unweighted__ networks without multiple neither self connections.

Consider, for example, a network with `N=5` vertices represented by:

```
1,2
1,3
2,4
2,5
3,4
```

Examples of datasets and their specifications are available at http://goo.gl/Bm3VsR.

## Installation

Python 3 is required, and also the [NumPy](http://www.numpy.org/) library.

## Use

If you want to manually input the dynamical parameters, just type:

```python dynamics.py <edges_file> <output_file>```

where ``<output_file>`` will be written with the average infected vertices density versus time.

Alternatively, use (Linux):

```bash run.sh <edges_file> <output_file> <number of samples> <infection rate lambda> <maximum time steps> <fraction of infected vertices (initial condition)>```

_Example:_

```bash run.sh edges/s01.edges.dat "s01.lb0.002_100-samples.dat" 100 0.002 1000000 0.5```

## License

This code is under [GNU General Public License v3.0](http://choosealicense.com/licenses/gpl-3.0/).

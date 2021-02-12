# Ecole vs Gasse et al. 2019

This repository contains the code to compare Ecole and
*[Exact combinatorial optimization with graph convolutional neural networks](http://papers.nips.cc/paper/9690-exact-combinatorial-optimization-with-graph-convolutional-neural-networks)*
Gasse, Chételat, Ferroni, Charlin, and Lodi (2019) in Advances in Neural Information Processing Systems (pp. 15580-15592).

## Setup
```bash
git submodule update --init --recursive
conda env create --name ecole_vs_gasse --file environment.yaml
conda activate ecole_vs_gasse
conda env update --file "vendor/ecole/dev/conda.yml"
cmake -B ecole_build -S vendor/ecole -D ECOLE_BENCHMARK=ON
cmake --build ecole_build --parallel
pip install ecole_build/python
pip install .
```

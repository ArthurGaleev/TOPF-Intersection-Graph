# TOPF-Intersection-Graph

The diploma on Topological Point Cloud Clustering method (V.P.Grande and M.T.Schaub, [2023](https://arxiv.org/abs/2303.16716)). The work investigated compatibility of topological features (V.P.Grande and M.T.Schaub, [2025](https://arxiv.org/abs/2406.02300)) and cap/cup products with KMeans, Deep Embedding Clustering (Xie et al., [2016](https://arxiv.org/abs/1511.06335)), Contrastive Clustering  (Le et al., [2020](https://arxiv.org/abs/2009.09687)) algorithms on [MNIST](https://docs.pytorch.org/vision/stable/generated/torchvision.datasets.MNIST.html#torchvision.datasets.MNIST) and [CIFAR10](https://docs.pytorch.org/vision/stable/generated/torchvision.datasets.CIFAR10.html#torchvision.datasets.CIFAR10) datasets in [`diploma_experiments.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/diploma_experiments.ipynb). Also intersection graphs were built on the top of my own implementation in [`my_topf_intersection_graphs.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/my_topf_intersection_graphs.ipynb) and on the top of topf (Grande et al., [2025](https://arxiv.org/abs/2406.02300)) [python package](https://pypi.org/project/topf/) in [`topf_intersection_graphs.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/topf_intersection_graphs.ipynb).

For a brief visual summary of the project's methodology and key results, check out the **[`poster.pdf`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/poster.pdf)**.

Obtained results:
<table>
  <thead>
    <tr>
      <th rowspan="2" align="center"><strong>Clustering</strong></th>
      <th rowspan="2" align="center"><strong>TOPF</strong></th>
      <th rowspan="2" align="center"><strong>CAP</strong></th>
      <th rowspan="2" align="center"><strong>CUP</strong></th>
      <th colspan="5" align="center"><strong>MNIST</strong></th>
      <th colspan="5" align="center"><strong>CIFAR10</strong></th>
    </tr>
    <tr>
      <th align="center"><strong>ACC</strong></th>
      <th align="center"><strong>NMI</strong></th>
      <th align="center"><strong>ARI</strong></th>
      <th align="center"><strong>FMI</strong></th>
      <th align="center"><strong>BCubed</strong></th>
      <th align="center"><strong>ACC</strong></th>
      <th align="center"><strong>NMI</strong></th>
      <th align="center"><strong>ARI</strong></th>
      <th align="center"><strong>FMI</strong></th>
      <th align="center"><strong>BCubed</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5" align="center"><strong>Kmeans</strong></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.79</td>
      <td align="center">0.78</td>
      <td align="center">0.71</td>
      <td align="center">0.75</td>
      <td align="center">0.76</td>
      <td align="center">0.25</td>
      <td align="center">0.13</td>
      <td align="center">0.07</td>
      <td align="center">0.17</td>
      <td align="center">0.17</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.8</td>
      <td align="center">0.79</td>
      <td align="center">0.73</td>
      <td align="center">0.76</td>
      <td align="center">0.78</td>
      <td align="center">0.25</td>
      <td align="center">0.13</td>
      <td align="center">0.07</td>
      <td align="center">0.17</td>
      <td align="center">0.17</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center"><strong>0.86</strong></td>
      <td align="center"><strong>0.79</strong></td>
      <td align="center"><strong>0.75</strong></td>
      <td align="center"><strong>0.78</strong></td>
      <td align="center"><strong>0.78</strong></td>
      <td align="center">0.25</td>
      <td align="center">0.13</td>
      <td align="center">0.07</td>
      <td align="center">0.17</td>
      <td align="center">0.17</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center">✓</td>
      <td align="center"><strong>0.86</strong></td>
      <td align="center"><strong>0.79</strong></td>
      <td align="center"><strong>0.75</strong></td>
      <td align="center"><strong>0.78</strong></td>
      <td align="center"><strong>0.78</strong></td>
      <td align="center"><strong>0.27</strong></td>
      <td align="center"><strong>0.13</strong></td>
      <td align="center"><strong>0.08</strong></td>
      <td align="center"><strong>0.17</strong></td>
      <td align="center"><strong>0.17</strong></td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">0.86</td>
      <td align="center">0.79</td>
      <td align="center">0.75</td>
      <td align="center">0.78</td>
      <td align="center">0.78</td>
      <td align="center">0.27</td>
      <td align="center">0.13</td>
      <td align="center">0.08</td>
      <td align="center">0.17</td>
      <td align="center">0.17</td>
    </tr>
    <tr>
      <td rowspan="5" align="center"><strong>DEC</strong></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.87</td>
      <td align="center">0.87</td>
      <td align="center">0.83</td>
      <td align="center">0.84</td>
      <td align="center">0.87</td>
      <td align="center">0.2</td>
      <td align="center">0.07</td>
      <td align="center">0.04</td>
      <td align="center">0.2</td>
      <td align="center">0.19</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.85</td>
      <td align="center">0.86</td>
      <td align="center">0.81</td>
      <td align="center">0.83</td>
      <td align="center">0.86</td>
      <td align="center">0.19</td>
      <td align="center">0.08</td>
      <td align="center">0.04</td>
      <td align="center">0.22</td>
      <td align="center">0.2</td>
    </tr>
      <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center">0.83</td>
      <td align="center">0.86</td>
      <td align="center">0.8</td>
      <td align="center">0.82</td>
      <td align="center">0.85</td>
      <td align="center">0.19</td>
      <td align="center">0.07</td>
      <td align="center">0.04</td>
      <td align="center">0.21</td>
      <td align="center">0.19</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center">✓</td>
      <td align="center">0.83</td>
      <td align="center">0.86</td>
      <td align="center">0.8</td>
      <td align="center">0.82</td>
      <td align="center">0.85</td>
      <td align="center">0.2</td>
      <td align="center">0.08</td>
      <td align="center">0.04</td>
      <td align="center">0.21</td>
      <td align="center">0.19</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">0.87</td>
      <td align="center">0.84</td>
      <td align="center">0.81</td>
      <td align="center">0.83</td>
      <td align="center">0.83</td>
      <td align="center">0.2</td>
      <td align="center">0.08</td>
      <td align="center">0.04</td>
      <td align="center">0.21</td>
      <td align="center">0.19</td>
    </tr>
    <tr>
      <td rowspan="5" align="center"><strong>CC</strong></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.57</td>
      <td align="center">0.47</td>
      <td align="center">0.4</td>
      <td align="center">0.46</td>
      <td align="center">0.47</td>
      <td align="center">0.22</td>
      <td align="center">0.09</td>
      <td align="center">0.05</td>
      <td align="center">0.14</td>
      <td align="center">0.14</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center">0.61</td>
      <td align="center">0.47</td>
      <td align="center">0.42</td>
      <td align="center">0.48</td>
      <td align="center">0.48</td>
      <td align="center">0.22</td>
      <td align="center">0.08</td>
      <td align="center">0.05</td>
      <td align="center">0.14</td>
      <td align="center">0.14</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center">0.61</td>
      <td align="center">0.49</td>
      <td align="center">0.44</td>
      <td align="center">0.5</td>
      <td align="center">0.5</td>
      <td align="center">0.22</td>
      <td align="center">0.09</td>
      <td align="center">0.05</td>
      <td align="center">0.14</td>
      <td align="center">0.15</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center"></td>
      <td align="center">✓</td>
      <td align="center"><strong>0.66</strong></td>
      <td align="center"><strong>0.5</strong></td>
      <td align="center"><strong>0.47</strong></td>
      <td align="center"><strong>0.52</strong></td>
      <td align="center"><strong>0.52</strong></td>
      <td align="center">0.22</td>
      <td align="center">0.09</td>
      <td align="center">0.04</td>
      <td align="center">0.14</td>
      <td align="center">0.14</td>
    </tr>
    <tr>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">✓</td>
      <td align="center">0.61</td>
      <td align="center">0.47</td>
      <td align="center">0.43</td>
      <td align="center">0.49</td>
      <td align="center">0.48</td>
      <td align="center">0.22</td>
      <td align="center">0.09</td>
      <td align="center">0.05</td>
      <td align="center">0.14</td>
      <td align="center">0.14</td>
    </tr>
  </tbody>
</table>

## Dependencies
All 3 notebooks with experiments use Python packages [`NumPy`](https://numpy.org), [`SciPy`](https://scipy.org), [`Pandas`](https://pandas.pydata.org), [`PyTorch`](https://pytorch.org), [`Scikit-learn`](https://scikit-learn.org/stable/), [`Gudhi`](https://gudhi.inria.fr), [`Matplotlib`](https://matplotlib.org) and [`Plotly`](https://plotly.com).

[`topf_intersection_graphs.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/topf_intersection_graphs.ipynb) used the [`TopF`](https://pypi.org/project/topf/) package itself, while [`diploma_experiments.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/diploma_experiments.ipynb) used a slightly modified version of it to add an extra output of [`topfmain`](https://github.com/vincent-grande/topf/blob/main/src/topf/topfmain.py) function for cap/cup products calculation.
To run them you need to set up [Julia locally](https://julialang.org/) or use colab/kaggle with pre-installed Julia. For both options you will need a specific Julia environment files from [topf repo](https://github.com/vincent-grande/topf/tree/main), you can take it from there or just download via `gdown` the [ready-to-run copy](https://drive.google.com/drive/folders/1jRYXgERnZF9EtJyE-g1k7I_UucAK_9Ff?usp=sharing) of it.

## Pretrained files
You can download the exact topological features used in [`diploma_experiments.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/diploma_experiments.ipynb) from [here](https://drive.google.com/drive/folders/1DM4ap4YIMldsxNKBc7QxNf5OQXPjnRYd?usp=sharing).

You can dwonload the pretrained autoencoder for MNIST and CIFAR10 used in [`diploma_experiments.ipynb`](https://github.com/ArthurGaleev/TOPF-Intersection-Graph/blob/main/diploma_experiments.ipynb)from [here](https://drive.google.com/drive/folders/1toL95sE2WOSii4pvJ-HOFqvBm-le72gs?usp=sharing).

## References
- Vincent P.Grande and Michael T.Schaub. Topological Point Cloud Clustering. In *40th International Conference on Machine Learning (ICML)*, 2023.
- Vincent P.Grande and Michael T.Schaub. Point-Level Topological Representation Learning on Point Clouds. In *42nd International Conference on Machine Learning (ICML)*, 2025.


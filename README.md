# Robust gradient descent via back-propagation: A Chainer-based tutorial

Here in this small repository, we provide a working example of a straightforward way to implement "robust gradient descent" learning algorithms for almost any neural network architecture using <a href="https://chainer.org/">Chainer</a>.

#### Demo code

The core demonstration used in this tutorial is a numerical experiment evaluating the utility of robust gradient descent methods applied to neural networks, under the possibility of arbitrary outliers. This demo is included in the Jupyter notebook file <a href="https://nbviewer.jupyter.org/github/feedbackward/chainrob/blob/master/demo.ipynb">demo.ipynb</a> (rendered using nbviewer).

#### Tutorial

In addition to the software in this library, we provide a <a href="LINK">step-by-step tutorial</a> which attempts to bridge the gap between the code and the concepts.

#### Related papers

Finally, here are some links to our research papers that take an in-depth look 
the robust gradient descent technique.

 - <a href="https://arxiv.org/abs/1706.00182">Efficient learning with robust gradient descent</a>. Matthew J. Holland and Kazushi Ikeda. Machine Learning (to appear), 2019.

 - <a href="https://arxiv.org/abs/1810.06207">Robust descent using smoothed multiplicative noise</a>. Matthew J. Holland. AISTATS 2019 (to appear).


#### Setup

The above demo was tested using Python 3.6 and Chainer 5.3.0. The basic software required can be assembled in a convenient manner using `conda`. Assuming the user has `conda` installed, run the following.

```
$ conda update -n base conda
$ conda create -n chainrob python=3.6 scipy scikit-learn chainer jupyter pip matplotlib
$ conda activate chainrob
(chainrob) $ pip install Cython
(chainrob) $ pip install --ignore-installed --upgrade chainer
(chainrob) $ pip install environment_kernels
```

Additionally, working with graph visualizations in Chainer, the output is in a standardized graph data format, called "DOT", with extension `.dot`. To work with files of this form, the `graphviz` utility is extremely useful. First install using

```
$ sudo apt install graphviz
```

and then to actually get to work, execute the following commands

```
$ conda activate chainrob
(chainrob) $ jupyter notebook
```

and subsequently select `demo.ipynb` from the list of files shown in-browser.
With that, all should be good to go.


__Author and maintainer:__<br>
<a href="https://feedbackward.com/">Matthew J. Holland</a> (Osaka University, ISIR)

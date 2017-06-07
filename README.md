<<<<<<< HEAD
# &nbsp; ![Ape is not a monkey][gorila] Neural Monkey

Neural Sequence Learning Using TensorFlow

[![Build Status](https://travis-ci.org/ufal/neuralmonkey.svg?branch=master)](https://travis-ci.org/ufal/neuralmonkey)
[![Documentation Status](https://readthedocs.org/projects/neural-monkey/badge/?version=latest)](http://neural-monkey.readthedocs.io/en/latest/?badge=latest)

The _Neural Monkey_ package provides a higher level abstraction for sequential
neural network models, most prominently in Natural Language Processing (NLP).
It is built on [TensorFlow](http://tensorflow.org/). It can be used for fast
prototyping of sequential models in NLP which can be used e.g. for neural
machine translation or sentence classification.

The higher-level API brings together a collection of standard building blocks
(RNN encoder and decoder, multi-layer perceptron) and a simple way of adding new
building blocks implemented directly in TensorFlow.

## Usage

```bash
neuralmonkey-train <EXPERIMENT_INI>
neuralmonkey-run <EXPERIMENT_INI> <DATASETS_INI>
neuralmonkey-server <EXPERIMENT_INI> [OPTION] ...
neuralmonkey-logbook --logdir <EXPERIMENTS_DIR> [OPTION] ...
```

## Installation

- You need Python 3.5.2 (or higher) to run _Neural Monkey_.

- When using virtual environment, execute these commands to install the Python
  dependencies:

  ```bash
  $ source path/to/virtualenv/bin/activate

  # For GPU-enabled version
  (virtualenv)$ pip install --upgrade -r requirements-gpu.txt

  # For CPU-only version
  (virtualenv)$ pip install --upgrade -r requirements.txt
  ```

- If you are using the GPU version, make sure that the `LD_LIBRARY_PATH`
  environment variable points to `lib` and `lib64` directories of your CUDA and
  CuDNN installations. Similarly, your `PATH` variable should point to the `bin`
  subdirectory of the CUDA installation directory.

- If the training crashes on an unknown dependency, just install it with
  pip. Remember to keep your virtual environment up-to-date with the package
  requirements file, which may be changed over time. To update the dependencies,
  re-run the `pip install` command from above (pay attention to the distinction
  between GPU and non-GPU versions).

## Getting Started

There is a
[tutorial](http://neural-monkey.readthedocs.io/en/latest/tutorial.html) that
you can follow, which gives you the overwiev of how to design your experiments
with Neural Monkey.

## Package Overview

- `bin`: Directory with neuralmonkey executables

- `examples`: Example configuration files for ready-made experiments

- `lib`: Third party software

- `neuralmonkey`: Python package files

- `scripts`: Directory with tools that may come in handy. Note dependencies for
   these tools may not be listed in the project requirements.

- `tests`: Test files

## Documentation

You can find the API documentation of this package
[here](http://neural-monkey.readthedocs.io/en/latest). The documentation files
are generated from docstrings using
[autodoc](http://www.sphinx-doc.org/en/stable/ext/autodoc.html) and
[Napoleon](https://sphinxcontrib-napoleon.readthedocs.io/en/latest/) extensions
to the Python documentation package
[Sphinx](http://www.sphinx-doc.org/en/stable/). The docstrings should follow
the recommendations in the [Google Python Style
Guide](http://google.github.io/styleguide/pyguide.html?showone=Comments#Comments).
Additional details on the docstring formatting can be found in the Napoleon
documentation as well.

## Related projects

- [tflearn](https://github.com/tflearn/tflearn) – a more general and less
  abstract deep learning toolkit built over TensorFlow

- [nlpnet](https://github.com/erickrf/nlpnet) – deep learning tools for
  tagging and parsing

- [NNBlocks](https://github.com/brmson/NNBlocks) – a library build over Theano
  containing NLP specific models

- [Nematus](https://github.com/rsennrich/nematus) - A tool for training and
  running Neural Machine Translation models

- [seq2seq](https://github.com/google/seq2seq) - a general-purpose
  encoder-decoder framework for Tensorflow

- [OpenNMT](https://github.com/opennmt/opennmt) - open sourcce NMT in Torch

## Citation

If you use the tool for academic purporses, please consider citing
[the following paper](https://ufal.mff.cuni.cz/pbml/107/art-helcl-libovicky.pdf):

```bib
@article{NeuralMonkey:2017,
    author = {Jind{\v{r}}ich Helcl and Jind{\v{r}}ich Libovick{\'{y}}},
    title = {Neural Monkey: An Open-source Tool for Sequence Learning},
    journal = {The Prague Bulletin of Mathematical Linguistics},
    year = {2017},
    address = {Prague, Czech Republic},
    number = {107},
    pages = {5--17},
    issn = {0032-6585},
    doi = {10.1515/pralin-2017-0001},
    url = {http://ufal.mff.cuni.cz/pbml/107/art-helcl-libovicky.pdf}
}
```

## License

The software is distributed under the [BSD
License](https://opensource.org/licenses/BSD-3-Clause).

[gorila]: http://ufallab.ms.mff.cuni.cz/~helcl/gorila3.png
=======
# LDNMT
LDNMT
Original code based on neuralmonkey https://github.com/ufal/neuralmonkey

# BPE Generation
paste ./examples/data/translation/train.en ./examples/data/translation/train.de | ./lib/subword_nmt/learn_bpe.py -s 50000  > ./examples/data/translation/merge_file.bpe
# training
bin/neuralmonkey-train exp-nm-mt/translation.ini

>>>>>>> 1aebc014cdc2e78cf764b2e09266770605b19e24

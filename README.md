# uSIF 

This is an implementation of *unsupervised smoothed inverse frequency* (uSIF), a simple but effective way to create sentence embeddings without any labelled data (Best Paper, Repl4NLP @ ACL 2018). See [the paper](http://aclweb.org/anthology/W18-3012) for more details.

\*01/11/18 Code now works for Python3 instead of Python2. 

### Setup

1. Unzip the pre-trained ParaNMT word vectors (thanks to John Wieting for providing this).
1. Install the python packages in requirements.txt.
1. Initialize a uSIF embedding model with usif.py. Call `get_paranmt_usif` to get the model that uses the ParaNMT vectors and call `test_STS` to see if you get the expected results. Once you know it's working, feel free to try it with other word vectors.

### Embedding Individual Sentences

If you don't have a sizable list of related sentences to embed, then there is not much point to doing piecewise common component removal, in which case you can set `m = 0` when initializing uSIF. Even for STS tasks, setting `m = 0` only decreases performance by 1 - 4%. 

### Reference

If you use this code, please cite
```
@article{ethayarajh2018unsupervised,
  title={Unsupervised Random Walk Sentence Embeddings: A Strong but Simple Baseline},
  author={Ethayarajh, Kawin},
  journal={ACL 2018},
  pages={91},
  year={2018}
}
```

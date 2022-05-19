# Learning Data Manipulation for Augmentation and Weighting

## 1. URL and BIB
https://arxiv.org/abs/1910.12795
```bibtex
@article{DBLP:journals/corr/abs-1910-12795,
  author    = {Zhiting Hu and
               Bowen Tan and
               Ruslan Salakhutdinov and
               Tom M. Mitchell and
               Eric P. Xing},
  title     = {Learning Data Manipulation for Augmentation and Weighting},
  journal   = {CoRR},
  volume    = {abs/1910.12795},
  year      = {2019},
  url       = {http://arxiv.org/abs/1910.12795},
  eprinttype = {arXiv},
  eprint    = {1910.12795},
  timestamp = {Fri, 01 Nov 2019 17:48:03 +0100},
  biburl    = {https://dblp.org/rec/journals/corr/abs-1910-12795.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```

## 2. Common data manipulation methods 

- argumentation:

  - image flipping
  - replace words with synonyms

- weighting

  - inverse class frequency (?)

  - loss values

previous work:
1. learn the composition of argumentation operations with RL
2. derive sample weights adaptively from a validation set via meta learning (?)
3. learn a weighting network by inducing a curriculum (?)

limited application scope

-> a new approach for different manipulation schemes

## 3. Ideas
- The main idea of the paper is to perform data augmentation and weighting by learning methods of data manipulation. 
	1. The corresponding relationship of x—>y in the data set should be regarded as a kind of policy
	2. The policy of the training set can be combined with the reward function in RL, so that changing the reward function can be regarded as rewarding different policies. 
	3. In this way, the two tasks of training the predictive model and manipulating the data can be carried out simultaneously.
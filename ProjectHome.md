# disfluency-detection-tool.tar.gz #
This is an off the shelf disfluency detector that takes one sentence per line in a input file, and output the POS tags and disfluency tags of each word. Read README for installation and running.


# naaclcode-v2.tar.gz #
The second version corrected the data preprocessing part in the first version. Now the data preprocessing procedure is exactly the same as Mark Johnson's implementation (1). (All words are in lower case, partial words are removed i.e., words whose POS tags are XX, or end in -, e.g., detectio- , spac-).

Now the performance is **0.8344** F score on development dataset and **0.8383** F score on test dataset.

The author would like to thank Matthew Honnibal and Haofeng Zhou for pointing the issues of previous version and their valuable suggestions.



(1) Simon Zwarts; Mark Johnson, The impact of language models and loss functions on repair disfluency detection, in Proc. of ACL 2011


# naaclcode.tar.gz #
Detecting disfluencies in spontaneous speech can be used to clean up speech transcripts.

There are two types of disfluencies: filler words  and edited words which are repeated or corrected by the following words. For example, `I want a flight to Boston, uh I mean, to Denver`. Where `to Boston` are edited words, and `uh I mean` are filler words.

Automatic filler word detection is much more accurate than edit detection, we focus on edited word detection.

This package recovers the highest performance (F=84.1%) on standard Switchboard corpus reported in our NAACL paper (1). It has been tested on platform: gcc version 4.4.4 20100630 (Red Hat 4.4.4-10) (GCC), it is not guaranteed to be runable on other platforms.

If you feel this package is helpful, we appreciate if you cite the paper

(1) Xian Qian and Yang Liu, Disfluency Detection Using Multi-step Stacked Learning, NAACL 2013.
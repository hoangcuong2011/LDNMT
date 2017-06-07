LDNMT

LDNMT Original code based on neuralmonkey https://github.com/ufal/neuralmonkey

BPE Generation

paste ./examples/data/translation/train.en ./examples/data/translation/train.de | ./lib/subword_nmt/learn_bpe.py -s 50000 > ./examples/data/translation/merge_file.bpe

training

bin/neuralmonkey-train exp-nm-mt/translation.ini

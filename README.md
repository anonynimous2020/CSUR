# CSUR code for Continual Learning for Sentiment Classification with AdaptiveUncertainty Regularization

## you need to download the pretrain model named bert-base-uncased in https://github.com/huggingface/transformers, and set it into data/bert-base-uncased

### you can run CSAR model use:
```
$ CUDA_VISIBLE_DEVICES=0 python main.py --approach CSUR --alpha 0.1 --beta 0.1 --gamma 0.03 --logname $SEED'_CSUR' --seed 1
```

### you can run BERT in continual learning:
```
$ CUDA_VISIBLE_DEVICES=0 python main.py --approach BERT --alpha 0.1 --beta 0.1 --gamma 0.03 --logname $SEED'_BERT' --seed 1
```

### you can run BERT in Re-init:
```
$ CUDA_VISIBLE_DEVICES=0 python finetune.py --approach BERT --alpha 0.1 --beta 0.1 --gamma 0.03 --logname $SEED'_BERT' --seed 1
```
------


### Requirements

- Python >=3.6
- Pytorch 1.6.0+cu10.1 / CUDA 10.1
- transformers


Reference

BERT Base network is from https://github.com/huggingface/transformers

# DAU-Net

**DAU-Net: A Density-Adaptive Unified Attention Network for Long-Tail Fish Counting in Aquaculture**.

DAU-Net is designed for underwater fish counting under uneven density distributions. The model contains a density-adaptive unified attention framework, including HCFA for dense-region feature enhancement and SIPA for sparse-region background suppression.

## Requirements

```bash
python >= 3.9
pytorch >= 1.12
torchvision
timm
numpy
scipy
opencv-python
pillow
matplotlib
tqdm
wandb
```


## Training

```bash
python train.py \
  --dataset ugcd \
  --data_dir ./data/UGCD \
  --crop_size 256 \
  --batch_size 1 \
  --max_epoch 80 \
  --lr 1e-5 \
  --weight_decay 1e-4
```

For other datasets, replace `ugcd` and `./data/UGCD` with `ccd`, `dgcd`, and the corresponding data path.

## Testing

```bash
python test.py \
  --dataset ugcd \
  --data_dir ./data/UGCD \
  --resume ./ckpts/DAUNet/ugcd/best_model.pth \
  --crop_size 256
```



## License

This code is released for academic research purposes only.

# GUI for SAM2
A GUI tool for SAM2 video segmentation. This demo has to be run on a workstation with a screen.

## Guangqi TODO
- [ ] Figure out why there is resolution mismatch between input and output.

## Installation
You should install [SAM2](https://github.com/facebookresearch/segment-anything-2?tab=readme-ov-file) first.
I use `SAM2-GUI/checkpoints/sam2.1_hiera_large.pt`.
```
pip install -r requirements.txt
```

## Processing Custom Data

We highly encourage users to structure their data directories in the following way:
```
- data_root
    '- videos
    |   - seq1.mp4
    |   - seq2.mp4
[and/or]
    '- images
    |   - seq1
    |   - seq2
    '- ...
```
## Usage
```
python mask_app.py --root_dir [data_root]

# e.g.
python mask_app.py --root_dir data/sam2gui/241208 --checkpoint_dir checkpoints/sam2.1_hiera_large.pt --model_cfg configs/sam2.1/sam2.1_hiera_l.yaml
```
![gradio interface](asset/gradio_interface.png)
Please first click on "Get SAM features" and then start segmenting. Frequently refer to the original repo issue for some error shot.

## Acknowledge
The app is modified based on [shape-of-motion](https://github.com/vye16/shape-of-motion/?tab=readme-ov-file).
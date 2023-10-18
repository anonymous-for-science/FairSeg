# FairSeg

Our FairSeg Dataset can be accessed via this [link](https://drive.google.com/drive/folders/1vXxt9qONVgnjm1ei7uv0XtoJrqVhouPX?usp=sharing).

## Prerequisites
- Linux (We tested our codes on Ubuntu 18.04)
- Anaconda
- Python 3.7.11
- Pytorch 1.9.1


First, please run the following commands:
```
conda create -n FairSeg python=3.7.11
conda activate FairSeg
pip install -r requirements.txt
```


## Quick start

Here are the instructions: 

## Training
We use 2 NVIDIA A100 GPUs for training.

After downloading our FairSeg Dataset, please specify the root_dir to train the SAMed and run this command.
```bash
./train.sh
```
After finishing the SAMed training, finetune the pretrained SAMed using our proposed Fair Error-Bound Scaling loss. Please specify the pretrained lora_ckpt and root_dir path. Then run command below: 
```bash
./train_finetune.sh
```


## Testing

For testing, please specify the root_dir, attribute, path of pretrained lora checkpoint, and OUTPUT_DIR. Then run this command.
```bash
./test.sh
```


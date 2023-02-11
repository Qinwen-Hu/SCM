# SDCM: Spectral Dimension Compression Mapping
The official code for *Learnable spectral dimension compression mapping for full-band speech enhancement (2023)*, accepted by JASA-EL.

## Requirements
+ pytorch 1.7.1
+ librosa
+ soundfile
+ pesq
+ pystoi


## Usage
### Clone
`git clone https://github.com/Qinwen-Hu/SDCM.git`
### Data preparation
Download the VoiceBank-Demand dataset, modify the corresponding `yaml` document, and run `python Dataloader_vctk_demand.py` to split the data into clips.
### Training
Run `python train_fullsubp.py` or  `python train_dptfsnet.py`.
### Evaluate
**eg.**
Run:
```
python evaluate.py -m f_scm -c ./ckpt/fullsubp_scm/model.ckpt -N /data/ssd/vctk_demand/noisy_testset_wav -C /data/ssd/vctk_demand/clean_testset_wav -O ./vctk_demand_enhanced -d cpu
```

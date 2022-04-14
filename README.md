<h1 align="center">
  <b>PyTorch VAE</b><br>
</h1>

<p align="center">
      <a href="https://www.python.org/">
        <img src="https://img.shields.io/badge/Python-3.5-ff69b4.svg" /></a>
       <a href= "https://pytorch.org/">
        <img src="https://img.shields.io/badge/PyTorch-1.3-2BAF2B.svg" /></a>
       <a href= "https://github.com/AntixK/PyTorch-VAE/blob/master/LICENSE.md">
        <img src="https://img.shields.io/badge/license-Apache2.0-blue.svg" /></a>
         <a href= "https://twitter.com/intent/tweet?text=PyTorch-VAE:%20Collection%20of%20VAE%20models%20in%20PyTorch.&url=https://github.com/AntixK/PyTorch-VAE">
        <img src="https://img.shields.io/twitter/url/https/shields.io.svg?style=social" /></a>

</p>

**Update 04/14/2022:** This fork is written for supporting the Numerai's dataset

A collection of Variational AutoEncoders (VAEs) implemented in pytorch with focus on reproducibility. The aim of this project is to provide
a quick and simple working example for many of the cool VAE models out there. 

### Requirements
- Python >= 3.5
- PyTorch >= 1.3
- Pytorch Lightning >= 0.6.0 ([GitHub Repo](https://github.com/PyTorchLightning/pytorch-lightning/tree/deb1581e26b7547baf876b7a94361e60bb200d32))
- CUDA enabled computing device

### Installation
```
$ git clone https://github.com/AntixK/PyTorch-VAE
$ cd PyTorch-VAE
$ pip install -r requirements.txt
```

### Usage
```
$ cd PyTorch-VAE
$ python3 run.py --config configs/numerai_vae.yaml
```

**View TensorBoard Logs**
```
$ cd logs/<experiment name>/version_<the version you want>
$ tensorboard --logdir .
```

**Note:** The default dataset is Numerai's train set. You need to download the `train.parquet` file from the Numerai's API and set the path in the configs/numerai_vae.yaml file.

<!--
### TODO
- [x] VanillaVAE
- [x] Beta VAE
- [x] DFC VAE
- [x] MSSIM VAE
- [x] IWAE
- [x] MIWAE
- [x] WAE-MMD
- [x] Conditional VAE- [ ] PixelVAE
- [x] Categorical VAE (Gumbel-Softmax VAE)
- [x] Joint VAE
- [x] Disentangled beta-VAE
- [x] InfoVAE
- [x] LogCosh VAE
- [x] SWAE
- [x] VQVAE
- [x] Beta TC-VAE
- [x] DIP VAE
- [ ] Ladder VAE (Doesn't work well)
- [ ] Gamma VAE (Doesn't work well) 
- [ ] Vamp VAE (Doesn't work well)
-->

### License
**Apache License 2.0**

| Permissions      | Limitations       | Conditions                       |
|------------------|-------------------|----------------------------------|
| ✔️ Commercial use |  ❌  Trademark use |  ⓘ License and copyright notice | 
| ✔️ Modification   |  ❌  Liability     |  ⓘ State changes                |
| ✔️ Distribution   |  ❌  Warranty      |                                  |
| ✔️ Patent use     |                   |                                  |
| ✔️ Private use    |                   |                                  |


### Citation
```
@misc{Subramanian2020,
  author = {Subramanian, A.K},
  title = {PyTorch-VAE},
  year = {2020},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/AntixK/PyTorch-VAE}}
}
```
-----------

[vae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/vanilla_vae.py
[cvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/cvae.py
[bvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/beta_vae.py
[btcvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/betatc_vae.py
[wae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/wae_mmd.py
[iwae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/iwae.py
[miwae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/miwae.py
[swae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/swae.py
[jointvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/joint_vae.py
[dfcvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/dfcvae.py
[mssimvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/mssim_vae.py
[logcoshvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/logcosh_vae.py
[catvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/cat_vae.py
[infovae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/info_vae.py
[vqvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/vq_vae.py
[dipvae_code]: https://github.com/AntixK/PyTorch-VAE/blob/master/models/dip_vae.py

[vae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/vae.yaml
[cvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/cvae.yaml
[bbvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/bbvae.yaml
[bhvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/bhvae.yaml
[btcvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/betatc_vae.yaml
[wae_rbf_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/wae_mmd_rbf.yaml
[wae_imq_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/wae_mmd_imq.yaml
[iwae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/iwae.yaml
[miwae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/miwae.yaml
[swae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/swae.yaml
[jointvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/joint_vae.yaml
[dfcvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/dfc_vae.yaml
[mssimvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/mssim_vae.yaml
[logcoshvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/logcosh_vae.yaml
[catvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/cat_vae.yaml
[infovae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/infovae.yaml
[vqvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/vq_vae.yaml
[dipvae_config]: https://github.com/AntixK/PyTorch-VAE/blob/master/configs/dip_vae.yaml

[1]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/Vanilla%20VAE_25.png
[2]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_Vanilla%20VAE_25.png
[3]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/WAE_RBF_18.png
[4]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_WAE_RBF_19.png
[5]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/WAE_IMQ_15.png
[6]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_WAE_IMQ_15.png
[7]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/BetaVAE_H_20.png
[8]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_BetaVAE_H_20.png
[9]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/IWAE_19.png
[10]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_IWAE_19.png
[11]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/DFCVAE_49.png
[12]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_DFCVAE_49.png
[13]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/MSSIMVAE_29.png
[14]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_MSSIMVAE_29.png
[15]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/ConditionalVAE_20.png
[16]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_ConditionalVAE_20.png
[17]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/CategoricalVAE_49.png
[18]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_CategoricalVAE_49.png
[19]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/JointVAE_49.png
[20]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_JointVAE_49.png
[21]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/BetaVAE_B_35.png
[22]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_BetaVAE_B_35.png
[23]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/InfoVAE_31.png
[24]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_InfoVAE_31.png
[25]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/LogCoshVAE_49.png
[26]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_LogCoshVAE_49.png
[27]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/SWAE_49.png
[28]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_SWAE_49.png
[29]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/MIWAE_29.png
[30]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_MIWAE_29.png
[31]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_VQVAE_29.png
[33]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/BetaTCVAE_49.png
[34]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_BetaTCVAE_49.png
[35]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/DIPVAE_83.png
[36]: https://github.com/AntixK/PyTorch-VAE/blob/master/assets/recons_DIPVAE_83.png

[python-image]: https://img.shields.io/badge/Python-3.5-ff69b4.svg
[python-url]: https://www.python.org/

[pytorch-image]: https://img.shields.io/badge/PyTorch-1.3-2BAF2B.svg
[pytorch-url]: https://pytorch.org/

[twitter-image]:https://img.shields.io/twitter/url/https/shields.io.svg?style=social
[twitter-url]:https://twitter.com/intent/tweet?text=Neural%20Blocks-Easy%20to%20use%20neural%20net%20blocks%20for%20fast%20prototyping.&url=https://github.com/AntixK/NeuralBlocks


[license-image]:https://img.shields.io/badge/license-Apache2.0-blue.svg
[license-url]:https://github.com/AntixK/PyTorch-VAE/blob/master/LICENSE.md

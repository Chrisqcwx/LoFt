# Code of "CALoR: Towards Comprehensive Model Inversion Defense"

All example scripts are place in `scripts/ffhq256_facescrub224/`. To use these scripts, you need to modified the paths in the scripts according to your own settings. The dataset intrduction is in [this](./docs/datasets.md) file.

## Pretrain Models on MS-Celeb-1M

```bash
cd scripts/ffhq256_facescrub224/classifier
python pretrain_<model_name>.py
```

## Training Models on FaceScrub224

We provide different codes for the defense methods.
```bash
cd scripts/ffhq256_facescrub224/classifier
python <defense_method>.py
```

Specifically, our low-rank compression defense is implemented in `lrc.py`.

## Fine-tuning Models with Confidence Adaptation


```bash
cd scripts/ffhq256_facescrub224/classifier
python ca_ft.py
```

## Attacks

The IF and PLG attacks are implemented in `scripts/ffhq256_facescrub224/if_defense/` and `scripts/ffhq256_facescrub224/plg_defense/`.
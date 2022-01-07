# Super-Resolution
This is VRDL HW4, the proposed challenge is image super resolution.
## Environment
- Python 3.8.11
- Pytorch 1.9.1
- CUDA 11.1
- KAIR
```
# install KAIR requirements
pip install -r requirements.txt
```

## How to train
1. Download the given dataset from [Google Drive](https://drive.google.com/file/d/1GL_Rh1N-WjrvF_-YOKOyvq0zrV6TF4hb/view)
2. Make sure that train and test folder is place in the path as `options/swinir/train_swinir_sr_classical_modified.json` mentioned
3. Run this command:
```
python main_train_psnr.py --opt best/train_swinir_sr_classical_modified.json
``` 
## How to test
1. Download Model [here](https://drive.google.com/file/d/1ZAMI19C1m-kBj4CGRBfOImDKZ9t9MX5c/view?usp=sharing)
2. Run this command:
```
python main_test_swinir.py --task classical_sr --scale 3 --model_path <model_path> --folder_lq <test_image_path>
```
And will get results in `results/`

## Reference
- [KAIR](https://github.com/cszn/KAIR)
- [SwinIR](https://github.com/JingyunLiang/SwinIR)

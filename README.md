# Training 3D U-Net and Segment Anything Model (SAM) on MRI Knee Images for Meniscus Segmentation

Repo containing code where SAM was fine-tuned on IWOAI 2019 knee MRI data.
A 3D U-Net was also trained as a baseline.

This work was presented at **BMVC 2024**.

You can read the paper via:

- [BMVC 2024 proceedings](https://bmvc2024.org/proceedings/957/)
- [arXiv](http://www.arxiv.org/abs/2504.13340)

If you wish to cite this work, please reference the arXiv version:

```bibtex
@article{mills2025meniscus,
  title={Putting the Segment Anything Model to the Test with 3D Knee MRI - A Comparison with State-of-the-Art Performance},
  author={Mills, Oliver and Conaghan, Philip and Ravikumar, Nishant and Relton, Samuel},
  journal={arXiv preprint arXiv:2504.13340},
  year={2025},
  doi={10.48550/arXiv.2504.13340}
}
```

## Project Structure

- `src/`: Models, dataset classes, metrics, and utility functions.
- `scripts/`: Train scripts for the models.
- `notebooks/`: Jupyter notebooks for:
  - Testing training code
  - Performing inference on test data (`test_unet.ipynb`, `run_test_split_through_sam.ipynb`)
  - Extracting and visualizing results:
    - `Bland_Altman_Plots.ipynb`
    - `Dice_scores.ipynb`
    - `Hausdorff_Distance.ipynb`
- `data/`: Add your data here after cloning.
- `models/`: Put model checkpoints here.

## Model Checkpoints

The model checkpoints used for final results in the paper can be downloaded [here](https://drive.google.com/drive/folders/143-YOXvaGO6W-3zLVfv5uPWxdBqvXXc5?usp=drive_link)

## Contact
For any queries, please email [scojm@leeds.ac.uk](mailto:scojm@leeds.ac.uk)

Directory Tree:
```bash
.
├── LICENSE
├── README.md
├── data
│   └── data.md
├── knees.yml
├── models
│   └── models.md
├── notebooks
│   ├── Bland_Altman_Plots.ipynb
│   ├── Dice_scores.ipynb
│   ├── Hausdorff_Distance.ipynb
│   ├── convert_to_slices.ipynb
│   ├── run_test_split_through_sam.ipynb
│   ├── test_sam.ipynb
│   ├── test_sam_slice_files.ipynb
│   └── test_unet.ipynb
├── scripts
│   ├── hyperparams_sam.txt
│   ├── hyperparams_unet.txt
│   ├── train_SAM.py
│   ├── train_SAM_slices.py
│   └── train_UNet.py
└── src
    ├── datasets.py
    ├── metrics.py
    ├── model_SAM.py
    ├── model_UNet.py
    └── utils.py
```

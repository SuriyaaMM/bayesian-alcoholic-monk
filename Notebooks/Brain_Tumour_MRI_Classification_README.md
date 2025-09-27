# Brain Tumour MRI Classification
- Brain tumors are a serious health challenge worldwide, and early detection plays a key role in effective treatment. 
- MRI (Magnetic Resonance Imaging) is one of the most widely used techniques for diagnosing brain tumors because it provides detailed images of soft tissues in the brain.

## Resources
- [Dataset](https://www.kaggle.com/datasets/arwabasal/brain-tumor-mri-detection)

## Instructions 
- Image File Paths will be unordered. 
- It will be better to rename everything in the `no` & `yes` directory chronologically.
- You can change the dataset path in cell number `2`.
- From this point onwards, everything should be straightforward.

## Mathematical Modelling
### Per-Class Independent Gaussian Modelling
- This is Naive Assumption I (Corresponding to the code)
- We will assume the Image itself is Drawn from the Class Gaussian with Parameters $\mu$ & $\sigma$
- $P(\textbf{x} | C1) = N(\mu_{C1}, \sigma_{C1})$ & $P(\textbf{x} | C2) = N(\mu_{C2}, \sigma_{C2})$

### Per-Pixel Independent Gaussian Modelling
- This is Naive Assumption II (Corresponding to the code)
- We will assume each Pixel is Drawn from a Gaussian with Parameters $\mu$ & $\sigma$
- $P(\textbf{x}_j | C1) = N(\mu_{C1, j}, \sigma_{C1, j})$ & $P(\textbf{x}_j | C2) = N(\mu_{C2, j}, \sigma_{C2, j})$ where $j = \{1, 2, ..... d \}$ where $d$ is the dimension of the image (ravelled).

### Per-Pixel Independent Gaussian Modelling along Principle Component
- Same Assumptions as previous Model but this time, $d$ isn't the ravelled image dimension, but the number of principal directions.


### Results & Analysis

| Method                                   | Accuracy (%)           |
|------------------------------------------|------------------------|
| Per Class Gaussian                       | 60.78                 |
| Per Pixel Gaussian                       | 72.55                 |
| Per Pixel Gaussian (Along Principle Direction) | 70.59                 |

- This performance is expected as Per-Class Gaussian should be the worst of all the three, Per-Pixel should be better & Per-Pixel Along Principle Direction should be somewhat worse then Per Pixel along all the dimension
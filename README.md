# Python code for "Deep Learning for Massive MIMO CSI Feedback"
(c) 2018 Wang-Ting Shih and Chao-Kai Wen e-mail: sydney2317076@gmail.com and chaokai.wen@mail.nsysu.edu.tw

## Introdution
This repository contains the original models described in the paper "Deep Learning for Massive MIMO CSI Feedback" (https://ieeexplore.ieee.org/document/8322184/).


## Requirements
- Python 3.5(or 3.6)
- Keras (>=2.1.1)
- Tensorflow (>=1.4)
- Numpy

## Steps to start

### Step1. Download the Model
There are two models in the paper:
- CsiNet: **CSI** sensing (or encoder) and recovery (or decoder) **net**work
- CS-CsiNet: Only learns to recover CSI from CS random linear measurements

We also provide two types of code:
- onlytest: Only to reproduce the results which provide in the paper. Also, we provide the model and weight which we have trained in the folder called 'saved_model'.
- train: Training by yourself

### Step2. Data Preparation
Download the data from https://drive.google.com/drive/folders/1_lAMLk_5k1Z8zJQlTr5NRnSD6ACaNRtj?usp=sharing. After you got the data, put the data as shown below.
```
*.py
saved_model/
  *.h5
  *.json
data/
  *.mat
```

### Step3. Run the file
Now, you are ready to run any *.py to get the result.

## Result
The table shows same as the results in paper:

|   gamma  |  Methods  | Indoor |            | Outdoor |        |
|:--------:|:---------:|:------:|:----------:|:-------:|:------:|
|          |           |  NMSE  |     rho    |   NSME  |   rho  |
|    1/4   | LASSO     |  -7.59 |    0.91    |  -5.08  |  0.82  |
|          | BM3D-AMP  |  -4.33 |     0.8    |  -1.33  |  0.52  |
|          | TVAL3     | -14.87 |    0.97    |   -6.9  |  0.88  |
|          | CS-CsiNet | -11.82 |    0.96    |  -6.69  |  0.87  |
|          | CsiNet    | **-17.36** |   **0.99**   |  **-8.75**  |  **0.91**  |
|   1/16   | LASSO     |  -2.72 |     0.7    |  -1.01  |  0.46  |
|          | BM3D-AMP  |  0.26  |    0.16    |   0.55  |  0.11  |
|          | TVAL3     |  -2.61 |    0.66    |  -0.43  |  0.45  |
|          | CS-CsiNet |  -6.09 |    0.87    |  -2.51  |  0.66  |
|          | CsiNet    |  **-8.65** |    **0.93**    |  **-4.51**  |  **0.79**  |
|   1/32   | LASSO     |  -1.03 |    0.48    |  -0.24  |  0.27  |
|          | BM3D-AMP  |  24.72 |    0.04    |  22.66  |  0.04  |
|          | TVAL3     |  -0.27 |    0.33    |   0.46  |  0.28  |
|          | CS-CsiNet |  -4.67 |    0.83    |  -0.52  |  0.37  |
|          | CsiNet    |  **-6.24** |    **0.89**    |  **-2.81**  |  **0.37**  |
|   1/64   | LASSO     |  -0.14 |    0.22    |  -0.06  |  0.12  |
|          | BM3D-AMP  |  0.22  |    0.04    |  25.45  |  0.03  |
|          | TVAL3     |  0.63  |    0.11    |   0.76  |  0.19  |
|          | CS-CsiNet |  -2.46 |    0.68    |  -0.22  |  0.28  |
|          | CsiNet    |  **-5.84** |    **0.87**    |  **-1.93**  |  **0.59**  |

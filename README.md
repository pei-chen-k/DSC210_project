# DSC210 Final Project on Food Recipe Recommendation System
### by Masfiqur Rahaman, Pei-Chen Kuo, Wenyi Liu, Zeyi Wu
### Course: DSC 210: Numerical Linear Algebra
### Instructor: Dr. Tsui-wei Weng

#### Instructions:
Please make sure that the following libraries are installed in python 3 environment:
  - numpy
  - pandas
  - math
  - scipy
  - collections
  - matplotlib
  - time
  - csv

* **NLA approach - matrix factorization**
  - Open 210_project_MatrixFactorization.ipynb on Google Colab
  - Download interactions_train.csv, interactions_validation.csv, and interactions_test.csv and upload them as runtime's files of 210_project_MatrixFactorization.ipynb
  - Run all the cells of the notebook 210_project_MatrixFactorization.ipynb


* **SOTA approach - improved Jaccard similarity**
  - Please download interactions_train.csv and DSC210_SOTA.ipynb. 
  - Upload both files to Google Drive. 
  - Open DSC210_SOTA.ipynb in Google Colab and run all the cells of the notebook (will need to give permission to access Google Drive).

#### Results:

* **NLA approach - matrix factorization**

Training and Validation MSE with different values of hyperparameter n_factor:
<img width="572" alt="MSE_VS_nfactors" src="https://github.com/pei-chen-k/DSC210_project/assets/66982698/1a2626f1-b6a9-47a0-8df1-3e8be4a86d18">

How training MSE changes with epochs:
<img width="854" alt="MSE_VS_epochs" src="https://github.com/pei-chen-k/DSC210_project/assets/66982698/5b5dede9-e341-4359-b0f0-476faf531389">


* **SOTA approach - improved Jaccard similarity**

Comparing our four SOTA approaches’s MSE with original Jaccard similarity approach’s MSE
<img width="572" alt="MSE" src="https://github.com/pei-chen-k/DSC210_project/assets/114783428/d810b652-2299-4e82-ac55-a0d56a8ca9ed">

Comparing our four SOTA approaches’s run time with the original Jaccard similarity approach’s run time
<img width="572" alt="Run_Time" src="https://github.com/pei-chen-k/DSC210_project/assets/114783428/b0d33a74-6694-4500-96c5-1d77ae74de7b">


### Compare and contrast:

Our experiments showed that all four SOTA approaches have lower testing MSE and lower run time compared to the NLA approach.

| Aspect      | SOTA (RJAC_U) | SOTA (RJAC_D) | SOTA (RJAC_DUB) | SOTA (WRJAC_DUB) | NLA Approach           |
| :---:       | :---:         | :---:         | :---:           | :---:            | :---:                  |
| Training MSE| Not applicable| Not applicable| Not applicable  | Not applicable   | 0.016                  |
| Testing MSE | 1.019         | 1.022         | 1.018           | 1.018            |19.61 (1st) / 2.47 (2nd)|
| Run time    | 121.913s      | 123.175s      | 123.656s        | 129.773s         | 1543.14s               |


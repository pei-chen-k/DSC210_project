# DSC210 Final Project on Food Recipe Recommendation System
### by Masfiqur Rahaman, Pei-Chen Kuo, Wenyi Liu, Zeyi Wu
### Course: DSC 210: Numerical Linear Algebra
### Instructor: Dr. Tsui-wei Weng

#### Instructions:

(Example from sample project github readme. Need to change.)

* Ensure that the following libraries are installed in python 3 environment:
  - scikit-learn
  - tqdm
  - nltk
  - umap
  - matplotlib
  - seaborn
  - wordcloud

* Open Latent_Semantic_Analysis.ipynb and run all the cells of the notebook.

* **NLA approach - matrix factorization**


* **SOTA approach - improved Jaccard similarity**
  - Please download interactions_train.csv and DSC210_SOTA.ipynb. 
  - Upload both files to Google Drive. 
  - Open DSC210_SOTA.ipynb in Google Colab and run all the cells of the notebook (will need to give permission to access Google Drive).

#### Results:

* **NLA approach - matrix factorization**

(Example from sample project github readme. Need to change.)

Top 5 words for each of the topics:
<img width="828" alt="Screen Shot 2022-04-15 at 9 20 17 AM" src="https://user-images.githubusercontent.com/18485647/163595256-eaa19d1b-9c52-4cd2-9a63-b1dbcd728d23.png">

Distributions of top 3 topics to each document:
<p align="center">
<img width="33%" alt="Screen Shot 2022-04-15 at 9 19 11 AM" src="https://user-images.githubusercontent.com/18485647/163595137-f9ea7e72-1f20-417f-bad4-4161cfcbe2f3.png">
 <img width="33%" alt="Screen Shot 2022-04-15 at 9 20 03 AM" src="https://user-images.githubusercontent.com/18485647/163595234-1951d9bf-0a54-40ec-8002-50d0042be260.png">
 <img width="33%" alt="Screen Shot 2022-04-15 at 9 19 35 AM" src="https://user-images.githubusercontent.com/18485647/163595185-18ca8fcc-ef7d-48fe-b7a5-76bb485a80a2.png">
</p>
Visualized embedding of documents in 2-D space:
<img width="816" alt="Screen Shot 2022-04-15 at 9 23 07 AM" src="https://user-images.githubusercontent.com/18485647/163595568-e9d9fd26-986a-4c06-8bf8-3bfbb95dbc79.png">


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


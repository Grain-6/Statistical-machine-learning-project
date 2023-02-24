# statistical-machine-learning-project
Written by python, including multiple datasets and models


Part I. Classification on 20newsgroup Data


Data info: the goal is to classify the types of postings based on their context. The dataset is a tiny
version of the 20newsgroups data, with binary occurrence data for 100 key words across 16242 postings.
The file “wordlist.txt” lists the 100 key words. The file “documents.txt” is essentially a 16242x100
occurrence matrix where each row is corresponding to 1 posting and each column is corresponding to 1
keyword. The occurrence matrix has binary entries where the (i,j)-th entry is 1 if and only if the i-th posting
contains the j-th keyword. Since the occurrence matrix is extremely sparse, the “documents.txt” is a
sparse representation of the occurrence matrix. Basically, each line in “documents.txt” represents 1 nonzero
entry of the occurrence matrix. For instance, the first line of “documents.txt” is “1 23 1” which means
that the entry (1,23) of the occurrence matrix is 1, i.e., the 1st posting contains the 23th keyword.
The file “newsgroup.txt” has 16242 lines where i-th line stands for the group labels of i-th posting. There
are 4 different groups which means “comp.”, “rec.”, “sci.” and “talk.” respectively. The goal is predict the
type, i.e. 4 different group, of the posting based on the words in this posting.


Part II. Spectral Clustering (PCA + K-means)on 20newsgroup Data


Part III. Classification on MNIST Data (The dataset needs to be downloaded from the publice source)


Dataset: MNIST/train_resized.csv, MNIST/test_resized.csv
Description: train_resized.csv has 30000 rows and 145 columns, test.csv has 12000 rows and 145
columns. Each row is corresponding to 1 handwriting digits. The first column label denotes the actual
digit that can be 0,1,…,9. The remaining 144=12*12 column are the pixels of one image, so each
image is of size 12x12.


Note that the original image is of size 28x28. I have downsized it to 12x12 to make your computation
faster. As a result, the image pixel values are not 0 or 1 anymore.


Part IV. Additional Bonus


Try any other machine learning methods you know, not necessarily limited to this course, on this
MNIST dataset. Report the best test performance you can get, the model and the time cost of
training your model. How does it compare to part III?

Part V. Semi-supervised Classification on Cardiotocography Data Set


Dataset: CTG/CTG_Train_labeled.csv, CTG/CTG_Train_unlabeled.csv, CTG/CTG_test.csv
Description: 2126 fetal cardiotocograms (CTGs) were automatically processed and the respective
diagnostic features measured. The CTGs were also classified by three expert obstetricians and a
consensus classification label assigned to each of them. Classification was respect to a fatal state
(N,S P). Therefore, the dataset is used here for a 3-class classification task.


Attribute Information:


LB - FHR baseline (beats per minute)


AC - # of accelerations per second


FM - # of fetal movements per second


UC - # of uterine contractions per second


DL - # of light decelerations per second


DS - # of severe decelerations per second


DP - # of prolongued decelerations per second


ASTV - percentage of time with abnormal short term variability


MSTV - mean value of short term variability


ALTV - percentage of time with abnormal long term variability


MLTV - mean value of long term variability


Width - width of FHR histogram


Min - minimum of FHR histogram


Max - Maximum of FHR histogram


Nmax - # of histogram peaks


Nzeros - # of histogram zeros


Mode - histogram mode


Mean - histogram mean


Median - histogram median


Variance - histogram variance


Tendency - histogram tendency


NSP - fetal state class code (N=normal; S=suspect; P=pathologic)

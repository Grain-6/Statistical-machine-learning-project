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


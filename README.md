# Fasta2svm

python fasta2svm.py  
* 参数设置

|参数|取值|
|:-:|:-|  
|-trainfasta|xxx.fasta|    
|-trainword|训练集分词的文件名. default=trainword.txt|   
-trainpos|    	正例数  
-trainneg|       	反例数  
-traincsv|       	 default= train.csv  
-kmer/-k|       	 kmer分词的k取值. default=3  
-b     |               	当模型中不存在该词的词向量的时候用b填充，default=0  
-sg     |     		0:cbow   1:skip-gram .default =1 
-hs      |     	0:Negative Sampling   1:Hierarchical softmax .default=0  
-window_size|   	窗口大小  
-model      |	词向量文件名  default=model.model  
-hidden_size|    	词向量的维度， default=100  
-testfasta  | 	 xxx.fasta
-testword   |	测试集分词文件名字，default=testword.txt  
-testpos   | 	正例数  
-testneg  |		反例数  
-testcsv | 		default=test.csv  
-mms   |		   是否使用归一化. default=False    
-ss     | 		 是否使用标准化. default=False 
-cv   |		交叉验证折数  
-n_job   |		线程数 default=最大线程  
-splite/-s| 0:kmer splite; 1:normal splite .default=0
*********************************
* 必须设置的参数有三个  
-trainfasta  
-trainpos  
-trainneg  
*************************
### example  
* python fatsa2svm.py -trainfasta xxx.fasta  -trainpos num  -trainneg num
* python fatsa2svm.py -trainfasta xxx.fasta  -trainpos num  -trainneg num  -testfasta   -testpos num  -testneg num -mms True


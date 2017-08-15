# Image Search

## Feature
VLAD可以理解为是BOF和fisher vector的折中 
BOF是把特征点做kmeans聚类，然后用离特征点最近的一个聚类中心去代替该特征点，损失较多信息； 
Fisher vector是对特征点用GMM建模，GMM实际上也是一种聚类，只不过它是考虑了特征点到每个聚类中心的距离，也就是用所有聚类中心的线性组合去表示该特征点，在GMM建模的过程中也有损失信息； 

VLAD像BOF那样，只考虑离特征点最近的聚类中心，VLAD保存了每个特征点到离它最近的聚类中心的距离； 
像Fisher vector那样，VLAD考虑了特征点的每一维的值，对图像局部信息有更细致的刻画； 
而且VLAD特征没有损失信息。

## Search Method

Bloom filter

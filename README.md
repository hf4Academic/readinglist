### 推荐领域paper
#### 冷启动方向
1. Neural Collabarative Reasoning https://arxiv.org/pdf/2005.08129.pdf, 这是将逻辑推理加入nn的训练当中，是从“感知”perception 到“认知”recognition的一个重要的工作
2. Warm Up Cold-start Advertisements: Improving CTR Predictions via Learning to Learn ID Embeddings https://arxiv.org/pdf/1904.11547.pdf 基于meta-learning的思路来为新品训练embedding，对少样本更加的友好
3. Recommendation for New Users and New Items via Randomized Training and Mixture-of-Experts Transformation https://dl.acm.org/doi/pdf/10.1145/3397271.3401178  SIGIR2020, 还没来得及看
4. InterBERT: An Effective Multi-Modal Pretraining Approach via Vision-and-Language Interaction https://arxiv.org/pdf/2003.13198.pdf 使用多模态的数据进行召回，对挖掘一些新品有一些帮助。 还没来得及看
5. Airbnb的一篇arxiv，里面提到了说对于新品的统计的missing特征做补齐是有作用的。 Improving Deep Learning For Airbnb Search (https://arxiv.org/pdf/2002.05515.pdf)

#### 用户兴趣方向
1. Multi-Interest Network with Dynamic Routing for Recommendation at Tmall https://arxiv.org/pdf/1904.08030.pdf ， 这个是利用hilton的capsule network做的兴趣聚类的工作
2. User Behavior Retrieval for Click-Through Rate Prediction https://arxiv.org/pdf/2005.14171.pdf， 这个是sigir20年的一篇paper，讲使用memory nwtwork来建模用户长期兴趣的，可以搭配sigir18年的一篇Improving Sequential Recommendation with Knowledge-Enhanced Memory Networks https://ata2.cn-hangzhou.oss-cdn.aliyun-inc.com/acm/10.1145_3209978.3210017.pdf?spm=ata.13269422.0.0.d9c14853Fwsqmh&OSSAccessKeyId=5brTYsCF9kNTYdU5&Expires=1595302778&Signature=nN4vOYxhvB%2FAZsjGFQBF%2BN6xsdM%3D  来一起看  
3. Search-based User Interest Modeling with Lifelong Sequential Behavior Data for Click-Through Rate Prediction  https://arxiv.org/pdf/2006.05639.pdf 阿里广告paper1
4. MIMN: Practice on Long Sequential User Behavior Modeling for Click-Through Rate Prediction https://arxiv.org/pdf/1905.09248.pdf 阿里广告paper2
5. Learning Disentangled Representations for Recommendation https://arxiv.org/pdf/1910.14238.pdf 直观的思想就是学习两个相对来说解耦的向量，一个能够反映出用户的宏观的兴趣，比如要买某一类东西，另外一个是之前的通过用户的点击交互行为学出来的微观的向量，有了宏观的向量之后，用户的embedding表示会更加的鲁棒，可解释性也会变强 [NIPS 2019]

#### 公平性方向
1. Controlling Fairness and Bias in Dynamic Learning-to-Rank https://dl.acm.org/doi/pdf/10.1145/3397271.3401100 这个是SIRIR2020的best paper

### 推荐领域公开数据集
#### 冷启动方向
1. http://jmcauley.ucsd.edu/data/amazon/ 该数据集有用户的id， 买的东西的id， 1-5的评分， 同时有商品的一些属性的特征可以作为简单的feature，比如 价格等。 另外这个数据集有一个统计特征，就是salesRank， 表示是某一个大类下面的sales排第几。 广告的SIM paper引用了其中的Book数据集合
2. MovieLen系列: 这个数据集的格式是  <userid, itemid, rate, timestamp> , 可以用来做id embedding冷启动的paper，但是没有统计特征。 用户的特征有 userid::gender::age::occupation::zipcode, movie的特征有MovieID::Title::Genres(国内这边类似的数据集合有：Tencent CVR prediction dataset, 和 KDD Cup 2012 CTR prediction dataset for search ads)
3. 腾讯App安装推荐数据集（Tencent CVR prediction dataset for App recommendation） http://algo.qq.com/ 格式是<广告，用户，label表示转化与否>, 每个广告有6个类别属性： 广告id，广告类别，campaign ID, app ID, app size 和 app type, 用户的特征包括 性别，年龄，occupation， consumption ability, education level and city, 注： Warm Up Cold-start Advertisements: Improving CTR Predictions via Learning to Learn ID Embeddings 这篇paper用过这个数据集 
4. KDD Cup 2012 CTR prediction dataset for search ads: https://www.kaggle.com/c/kddcup2012-track2 。 格式是<UserID, AdID, Query, Depth, Position, Impression, Click>， 其中impression表示这个广告用户看了几次， click表示这个广告被这个用户看了几次， 别的特征就是用户的性别，年龄，query，title，description的对应的nlp文字的tokenid, 注意：arm Up Cold-start Advertisements: Improving CTR Predictions via Learning to Learn ID Embeddings 这篇paper用过这个数据集
5. Taobao Dataset. 天池kaggle比赛用了 https://tianchi.aliyun.com/dataset/dataDetail?dataId=649， 和MovieLen的数据集合相比没有太多的数据增量，唯一就是用户的行为包括展示，购买，加购，收藏。 timestamp这些 movielen也是有的，用来形成用户的行为序列

#### Learning to Rank方向
1. Yahoo! Learning to Rank Challenge C14, 也叫 https://webscope.sandbox.yahoo.com/catalog.php?datatype=c ， 这个数据数据集好处就是除了label之外，还有很多稠密的特征，虽然这些稠密的特征的描述都没有给。这个是一个搜索数据集，描述了每一个query下面的url是不是被点。有点类似于一个用户下面的item有没有被点，可以转化成推荐数据集来使用
2. 

### 其他一些工具网页
1. pandas教程，是我看的写的很好的 https://data36.com/pandas-tutorial-3-important-data-formatting-methods-merge-sort-reset_index-fillna/
2. 做论文图需要一些矢量的icon。 https://www.iconfont.cn/plus/collections/index?spm=a313x.7781069.1998910419.3.IwAAti

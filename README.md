### 推荐领域paper
#### 冷启动方向
1. Neural Collabarative Reasoning https://arxiv.org/pdf/2005.08129.pdf, 这是将逻辑推理加入nn的训练当中，是从“感知”perception 到“认知”recognition的一个重要的工作
2. Warm Up Cold-start Advertisements: Improving CTR Predictions via Learning to Learn ID Embeddings https://arxiv.org/pdf/1904.11547.pdf 基于meta-learning的思路来为新品训练embedding，对少样本更加的友好
3. Recommendation for New Users and New Items via Randomized Training and Mixture-of-Experts Transformation https://dl.acm.org/doi/pdf/10.1145/3397271.3401178  SIGIR2020, 还没来得及看
4. InterBERT: An Effective Multi-Modal Pretraining Approach via Vision-and-Language Interaction https://arxiv.org/pdf/2003.13198.pdf 使用多模态的数据进行召回，对挖掘一些新品有一些帮助。 还没来得及看

#### 用户兴趣方向
1. Multi-Interest Network with Dynamic Routing for Recommendation at Tmall https://arxiv.org/pdf/1904.08030.pdf ， 这个是利用hilton的capsule network做的兴趣聚类的工作
2. User Behavior Retrieval for Click-Through Rate Prediction https://arxiv.org/pdf/2005.14171.pdf， 这个是sigir20年的一篇paper，讲使用memory nwtwork来建模用户长期兴趣的，可以搭配sigir18年的一篇Improving Sequential Recommendation with Knowledge-Enhanced Memory Networks https://ata2.cn-hangzhou.oss-cdn.aliyun-inc.com/acm/10.1145_3209978.3210017.pdf?spm=ata.13269422.0.0.d9c14853Fwsqmh&OSSAccessKeyId=5brTYsCF9kNTYdU5&Expires=1595302778&Signature=nN4vOYxhvB%2FAZsjGFQBF%2BN6xsdM%3D  来一起看  
3. Search-based User Interest Modeling with Lifelong Sequential Behavior Data for Click-Through Rate Prediction  https://arxiv.org/pdf/2006.05639.pdf 阿里广告paper1
4. MIMN: Practice on Long Sequential User Behavior Modeling for Click-Through Rate Prediction https://arxiv.org/pdf/1905.09248.pdf 阿里广告paper2
5. Learning Disentangled Representations for Recommendation https://arxiv.org/pdf/1910.14238.pdf 直观的思想就是学习两个相对来说解耦的向量，一个能够反映出用户的宏观的兴趣，比如要买某一类东西，另外一个是之前的通过用户的点击交互行为学出来的微观的向量，有了宏观的向量之后，用户的embedding表示会更加的鲁棒，可解释性也会变强 [NIPS 2019]

#### 公平性方向
1. Controlling Fairness and Bias in Dynamic Learning-to-Rank https://dl.acm.org/doi/pdf/10.1145/3397271.3401100 这个是SIRIR2020的best paper

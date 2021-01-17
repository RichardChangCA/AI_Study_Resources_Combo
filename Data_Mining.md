Stanford CS246 Mining Massive Data Sets https://www.bilibili.com/video/BV1SC4y187x1/?spm_id_from=333.788.recommend_more_video.0

<b>Lecture 1 Introduction, MapReduce and Spark</b>

<b>Lecture 2 Frequent itemsets and Association rules</b>

Items: products, Baskets: sets of products someone bought in one trip to the store. A-Priori Algorithm limits the need for main memory: Key idea: monotonicity, if a set of items I appears at least s times, so does every subset J of I. Contrapositive for pairs: If item i does not appear in s baskets, then no pair including i can appear in s baskets(Pass 1: Read baskets and count in main memory the number of occurrences of each individual item, and items that appear larger than s times are the frequent items. Pass 2: Read baskets again and keep track of the count of only those pairs where both elements are frequent). 

https://zhuanlan.zhihu.com/p/43263751

## what's bloom filter
probabilistic data structure

## benefit
fast insert and query

## specificity
return is not exact

## delete support
NO

## select
k (hash function nnumber) and m (bloom filter len) n (numbers of inserted element), p (positives)
![](http://latex.codecogs.com/gif.latex?-\\frac{n\\ln p}{(ln2)^2})

## MurmurHash and Fnv 
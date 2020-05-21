# Empirical Study of Entity Resolution Using Word Embedding
## Table of Contents
- [Empirical Study of Entity Resolution Using Word Embedding](#empirical-study-of-entity-resolution-using-word-embedding)
  * [Abstract](#abstract)
  * [Proposed Approach](#proposed-approach)
    + [Overview](#overview)
    + [Unsupervised Approach](#unsupervised-approach)
      - [1. TF-IDF](#1-tf-idf)
      - [2. Random Index](#2-random-index)
      - [3. FastText Unsupervised CBOW + SkipGram](#3-fasttext-unsupervised-cbow---skipgram)
    + [Pre-Trained Approach](#pre-trained-approach)
      - [4. FastText CBOW (Common Crawl + Wikipedia)](#4-fasttext-cbow--common-crawl---wikipedia-)
      - [5. FastText SkipGram (Wikipedia)](#5-fasttext-skipgram--wikipedia-)
      - [6. FastText CBOW/SkipGram + Random Indexing](#6-fasttext-cbowskipgram--random-indexing)
    + [Further Experiments](#further-experiments)
      - [7. Combined Ranked List from Two best approach](#7-combined-ranked-list-from-two-best-approach)
      - [8. Concatenate Word Embeddings of Two best approach](#8-concatenate-word-embeddings-of-two-best-approach)
      - [9. Blocking using Manufacturer & Price of Top 3 Approach](#9-blocking-using-manufacturer---price-of-top-3-approach)
  * [Experimental Results](#experimental-results)
  * [Library and Pre-Trained Embedding](#library-and-pre-trained-embedding)
  * [Code](#code)
      - [Unsupervised Approaches](#unsupervised-approaches)
      - [Pre-Trained Approaches](#pre-trained-approaches)
      - [Further Experiments](#further-experiments-1)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'></a></i></small>

## Abstract
Entity Resolution was originally used to be solved through Deterministic Linkage Methods and Probabilistic Linkage Methods that simply matches identifiers from both record pairs and links them when they agree. With modern machine learning techniques applied to this problem, solutions such as string matching, string distance (Jaccard Similarity), graphical models, and etc have often improved the performance of many record linkage systems. Most of these modern machine learning solutions rely on a variation of string matching to link record pairs. This project is focused on solving this problem with the use of word embeddings that essentially captures the word’s meaning and represents it in a vector space. By using word semantic, the machines can now try to link records through the words meaning instead of by matching the letters of the string. This can help solve the problem of polysemy, where different words or phrases can have related meaning. Word embeddings can capture the difference in the meanings of the same word while string matching would not. Thus, word embedding can be a more general approach that can be applied to Entity Resolution problems in many different fields with an optimal performance.

## Proposed Approach
### Overview
### Unsupervised Approach
#### 1. TF-IDF
#### 2. Random Index
#### 3. FastText Unsupervised CBOW + SkipGram
### Pre-Trained Approach
#### 4. FastText CBOW (Common Crawl + Wikipedia)
#### 5. FastText SkipGram (Wikipedia)
#### 6. FastText CBOW/SkipGram + Random Indexing
### Further Experiments
#### 7. Combined Ranked List from Two best approach
#### 8. Concatenate Word Embeddings of Two best approach
#### 9. Blocking using Manufacturer & Price of Top 3 Approach 



## Experimental Results

## Library and Pre-Trained Embedding
FastText Python Installation:  
https://fasttext.cc/docs/en/support.html#building-fasttext-python-module

FastText Pre-Trained Word Vectors:  
CBOW: https://fasttext.cc/docs/en/crawl-vectors.html  
SkipGram: https://fasttext.cc/docs/en/pretrained-vectors.html  

## Code
#### Unsupervised Approaches
1. TF-IDF
    1. TF-IDF.ipynb
2. Random Indexing
    1. Random Indexing.ipynb
3. FastText Unsupervised (CBOW/SkipGram)
    1. FastText(Unsupervised).ipynb

#### Pre-Trained Approaches
4. FastText Wikipedia (CBOW)
    1. FastText (Wiki CBOW).ipynb
5. FastText Wikipedia (SkipGram):
    1. FastText (Wiki SkipGram).ipynb
6. FastText Wikipedia (CBOW/SkipGram) + Random Indexing
    1. Random Indexing (Pre-Trained CBOW).ipynb
    2. Random Indexing (Pre-Trained SkipGram).ipynb
    
#### Further Experiments
7. Combination of Ranked List (Average Cosine Similarity)
    1. TF-IDF + Pre-Trained (SkipGram) Cosine Similarity.ipynb
    2. Pre-Trained + Unsupervised (SkipGram) Cosine Similarity.ipynb
8. Word Embedding Concatenation
    1. TF-IDF + Pre-Trained (SkipGram) Vector Concat.ipynb
    2. Pre-Trained + Unsupervised (SkipGram) Vector Concat.ipynb
9. Blocking using Manufacturing and Price Fields
    1. FastText (Wiki SkipGram) + Blocking (-0.25).ipynb
    2. FastText (Wiki SkipGram) + Blocking (-3).ipynb
    3. TF-IDF + Pre-Trained (SkipGram) Vector Concat + Blocking (-0.25).ipynb	
    4. TF-IDF + Pre-Trained (SkipGram) Vector Concat + Blocking (-3).ipynb	

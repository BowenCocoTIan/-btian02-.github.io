---
layout: post
title: The Hash function
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

n the previous lectures in DSCI 511 , we see that if we have a list “L ”and we want to know whether certain element “x” is contained in the list, we could simply type “x in L ” in Python to retrieve a “True” or “False” response. In fact this is proceeded by using some binary search algorithm. Here we would like to further investigate this idea of searching by building a data structure that can be searched in O(1) time, which is called hashing.
Intuitively when we cook, to hash something means to chop it and then mix it. Like the hash browns, what we love most in the English breakfast , is the shredded and fried potato cuisine. In order to chop things , we need a chopping board to have a clear organization of the food we chopped ; in our case of hashing, we need a hash table. A hash table is a collection of items which are stored in a way in order to make it easy to find them later. Each position of the hash table, which is called a slot, is holding an item and often labelled by a non-negative integer .For example, we will have a slot labelled 0, a slot labelled 1, a slot labelled 3, and so on. Initially, the hash table contains no items so every slot is empty, and we implement it using Python by assigning an initial value “None”. Then the ultimate goal is to map the item that we are looking for , and slot that the item belongs to .
Hence a hash function intuitively is where a computer takes an input of data including letters, numbers, and symbols, then uses a mathematical formula to chop it, mix it up, and produce an output of a specific length which is the slot that we are looking for. A hash function is some function that can be used to map data of arbitrary size to some fixed-size values which are called hashes.
Each hash function chops up and mixes in different ways with different mathematical formulas and so will produce different hashes. As you may see, the mathematical formula in the hash function is the secrete “recipe”. There are numeric mathematical formulas for hash functions, and one of them is the folding method. The folding method for constructing hash functions begins by dividing the input into equal-size pieces (the last piece may not be of equal size). These pieces are then added together to give the resulting hash value. For example, if the input was the phone number 7807091655, we would divide the digits into groups of two (78,07,09,16,55). After the addition, 78+07+09+16+55, we get 165. Another mathematical formula is called the mid-square method. We use an example of number 33 with 11 slots to illustrate it. First we square the number 22 and we get 1089, then we take the middle two digits 08, apply the remainder algorithm with base 11, we retrieve the number 8.
These are some short illustration of the hash function. In the future hopefully we can explore the combinatorial techniques applied to the hash functions.
References. https://runestone.academy/runestone/books/published/pythonds/ SortSearch/Hashing.html
https://en.wikipedia.org/wiki/ Cryptographic_hash_function#Hash_functions_based_on_block_ ciphers
https://medium.com/tech-tales/what-is-hashing-6edba0ebfa67


The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

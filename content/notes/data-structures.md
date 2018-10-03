---
layout: notes
title: data structures
---

# functional
https://www.cs.cmu.edu/~rwh/theses/okasaki.pdf


# Arrays

# Stack

# Queue

# Linked List

## Singly

## Double

# Hash Table

A [hash table](https://github.com/dotnet/corefx/blob/9cb4ea0045eed954d72aea6f283d22f2d7fb3c7b/src/Common/src/CoreLib/System/Collections/Hashtable.cs) is a collection of key/value pairs that are organized on the hash code of the key. It's a data structure that maps keys to values for highly efficient lookup. Think of it along the lines of `data to a key, mapped to an data structure (array or balanced binary search tree) to distribute this data in a performant manner, backed by a linkedlist`. At linkedlist must be used because of hashing collisions, you could have two different keys with the same hashcode or two different hash codes that map to the same index.

1. compute the the keys hashcode, typically a long or an int. for example a key of `"hi"` hashing to `10320` long or int.
2. map the hash code to an index in the array. an example of this would be `hash(key) % array_length`. Note, two different keys with the same hashcode could map to the same index.
3. at the index there is linked list of keys and values. store the keys and values in this index. At linkedlist must be used because of collisions, you could have two different keys with the same hashcode or two different hash codes that map to the same index.

To retrieve the value pair by it's key, compute the hash code from they key, and compute the index from the hash code, then search through the linked list for the value with this key.

If the number of hashing collisions is very high, the worst case runtime performance is `O(n)`, where `n` is the number of keys. If we assume a good implementation where collisions are at a min the lookup time is `O(1)`. Hashing collisions can be reduced by using a techinque called [double hashing](https://en.wikipedia.org/wiki/Double_hashing)


## Collisions


# Dictionary

# Trees

## Binary Tree

## Heap

## Binary Search Tree

## Trie

# Graphs

## Directed and Undirected

## Weighted and Unweighted

## Cycles

## Directed Acyclic Graphs


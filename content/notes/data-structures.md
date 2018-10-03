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

A hash table is a data structure that maps keys to values for highly efficient lookup. Think of it along the lines of `data to a key, mapped to an array to distribute this data in a performant manner, backed by a linkedlist of key value pairs to deal with collisions`. At linkedlist must be used because of collisions, you could have two different keys with the same hashcode or two different hash codes that map to the same index.

1. compute the the keys hashcode, typically a long or an int. for example a key of `"hi"` hashing to `10320` long or int.
2. map the hash code to an index in the array. an example of this would be `hash(key) % array_length`. Note, two different keys with the same hashcode could map to the same index.
3. at the index there is linked list of keys and values. store the keys and values in this index. At linkedlist must be used because of collisions, you could have two different keys with the same hashcode or two different hash codes that map to the same index.

To retrieve the value pair by it's key, compute the hash code from they key, and compute the index from the hash code, then search through the linked list for the value with this key.

```
var backingArray = new LinkedList<KeyValuePair<TKey, TValue>>[127];
```

```csharp
void Main()
{
	// Create Dictionary.
    Dictionary<string, int> hash = new Dictionary<string, int>();

    // Add some data.
    hash.Add("diamond", 500);
    hash.Add("ruby", 200);
    hash.Add("pearl", 100);

    // Get value that exists.
    int value1 = hash["diamond"];
    Console.WriteLine("get DIAMOND: " + value1);

    // Get value that does not exist.
    hash.TryGetValue("coal", out int value2);
    Console.WriteLine("get COAL: " + value2);

    // Loop over items in collection.
    foreach (KeyValuePair<string, int> pair in hash)
    {
        Console.WriteLine("KEY: " + pair.Key);
        Console.WriteLine("VALUE: " + pair.Value);
    }
}
```

If the number of hashing collisions is very high, the worst case runtime performance is `O(n)`, where `n` is the number of keys. If we assume a good implementation where collisions are at a min the lookup time is `O(1)`.


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


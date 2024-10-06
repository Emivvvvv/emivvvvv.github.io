---
title: NeetCode 150 Cheatsheet
draft: false
tags:
---
# Introduction

As I mentioned in [[python-for-interviews-cheatsheet|Python for Interviews Cheatsheet]] post, I need to be prepared for the coding interviews. In this post, I'll be sharing the critical points for later use.

# NeetCode 150

NeetCode is originally a YouTube page that solves coding problems and gives some tutorials for improvement. NeetCode 150 specifically is the 150 LeetCode problems that he thinks are the most essential ones. NeetCode also has a website for preparing interviews which has some paid and some free content. I'll be focusing on free ones. On the website, there is a [[https://neetcode.io/roadmap|roadmap]] section that has the 150 questions that he mentioned with a suggested solving order. 

![NeetCode 150 roadmap](neetcode-roadmap.PNG)
I'll be following this. 

So let's go with the roadmap's order.

## Arrays & Hashing

### HashSet

Since sets don't allow duplicates, they can be useful in many cases. For example, you can easily check if there are duplicates in an array using this approach:

```python
len(set(nums)) < len(nums)
```

Checking a key is already present is also handy in a lot of cases

```python
nums = set()

if 31 in nums:
	...
```
### HashTable (Dictionary in Python)

To handle edge cases when accessing dictionary keys, use `.get()` with a default value instead of directly referencing the key with `[]`. For instance:

```python
countS[s[i]] = 1 + countS.get(s[i], 0)
```

In this example, if `countS[s[i]]` is not set, `.get()` will return `0` by default, preventing an error that would occur if you tried to access the key directly with `[]`.

It's also handy to create a dictionary where the values are collections:

```python
map_with_lists = defaultdict(list)
map_with_sets = defaultdict(set)
```

### General Tips

You can use `ord()` to get the ASCII value of a character. In this example, it's used as an index.

```python
for char in word:
	chars[ord(char) - ord('a')] += 1
```

HashSets and HashMaps (or dictionaries in Python) can only use immutable data types as keys. If you need to use a list as a key, convert it to a tuple first:

```python
key = tuple(my_list)
```

Creating a list with initial values can be easily done with:

```python
res = [1] * length
```

This will create a list of the specified `length` with all elements initialized to `1`.

## Two Pointers

## Binary Search

## Sliding Window

## Linked List

## Trees

## Tries

## Heap/Priority Queue

I'll update this post as I solve the questions...
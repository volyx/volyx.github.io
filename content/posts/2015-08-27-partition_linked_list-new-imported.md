---
author: "volyx"
title:  "Поделить связанный список по значению"
date: "2015-08-27"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: ""
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---


== Поделить связанный список по значению

# Задача
Дан связанный список и целое число //N// из этого списка. Поделить связный список вокруг одного узла, так чтобы узлы с меньшим значением находились до него, а узлы со значениями больше //N// после него.

# Решение

Решение похоже на 

This is much like the partition function for quick sort. When using arrays we have to be careful not to shift elements around, because array shifts are expensive operations. But when we use a linked list we don’t have to worry about this. We could have a list that stores all values less than N and a list that stores all values greater than N and equal to N. Then we can merge the 2 lists and the N node together to get the resulting list. Here is the outline for the algorithm

create 2 empty lists, one to store values smaller, other to store values greater
scan the list from head to tail
at each step if the current node is smaller than N append it to the smaller list
if the current node is larger than N append it to the larger list
append the list is complete append N and larger to the smaller list to have the final result
Here is the code

[source, java]
----
static LinkedListNode partition(LinkedListNode head, int v) {
        LinkedListNode smHead = null;
        LinkedListNode smTail = null;
 
        LinkedListNode gtHead = null;
        LinkedListNode gtTail = null;
 
        LinkedListNode cur = head;
        while(cur != null) {
            LinkedListNode next = cur.next;
            cur.next = null;
            if (cur.data < v) {
                if (smHead == null) {
                    smHead = cur;
                    smTail = smHead;
                } else {
                    smTail.next = cur;
                    smTail = cur;
                }
            } else {
                if (gtHead == null) {
                    gtHead = cur;
                    gtTail = gtHead;
                } else {
                    gtTail.next = cur;
                    gtTail = cur;
                }
            }
            cur = next;
        }
 
        if (smHead == null) return gtHead;
        smTail.next = gtHead;
        return smHead;
    }
----
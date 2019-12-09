# 堆排序

使用优先队列-最小/最大堆可实现。

## 优先队列

优先队列是一种能完成以下任务的队列：插入一个数值，取出最小的数值（获取数值，并且删除）。优先队列可以用二叉树来实现，我们称这种为二叉堆。

### 最小堆

最小堆是二叉堆的一种，是一颗完全二叉树（一种平衡树）， 其特点是父节点的键值总是小于或者等于子节点。

```
实现细节(两个操作)：

push：向堆中插入数据时，首先在堆的末尾插入数据，然后不断向上提升，直到没有大小颠倒时。
pop：从堆中删除最小值时首先把最后一个值复制到根节点上，并且删除最后一个数值。然后不断向下交换， 直到没有大小颠倒为止。在向下交换过程中，如果有两个子儿子都小于自己，就选择较小的

插入时间复杂度O(logN)，删除时间复杂度O(logN)，两个二叉堆合并时间复杂性O(NlogN).
```

最大堆同理。可用此结构实现堆排序算法。
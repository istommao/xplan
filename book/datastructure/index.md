# 数据结构

## 线性表

*什么是线性表?*

> 由同类型的数据元素构成的有序序列的线性结构

- 线性表的长度: 表中元素个数
- 空表: 线性表中没有元素
- 表头: 线性表起始位置
- 表尾: 表结束的位置

- [x]数组实现
- [x]链表实现

**数组实现**

```c
#define MAXSIZE 30;
typedef int ElementType;

typedef struct {
    ElementType data[MAXSIZE];
    int last;
} List;


List createList()
{
    List *P;
    P = (List *)malloc(sizeof(List));
    P->last = -1;
    return P;
}

int insertItem(ElementType item, int i, List *P)
{
    int j;
    if (P->last == MAXSIZE - 1) {
        printf("表已满")
        return -1;
    }
    if (i < 1 || i > P->last + 2) {
        printf("插入位置不合法");
        return -1;
    }
    for (j = P->last; j >= i - 1; j--)
        P->data[j+1] = P->data[j];
    P->data[i-1] = item;
    P->last++;
    return 1;
}

int findByItem(ElementType item, List *P)
{
    int i = 0;
    while (i <= P->last && P->data[i] != item)
        i++;

    if (i > P->last)
        return -1;
    else
        return i;
}
```


## 栈与队列

## 树与二叉树

- Tree 树
- Binary tree 二叉树
- Binary Search Tree 二叉查找树
- AVL 平衡二叉树
- Red–black tree 红黑树

## 图

- BFS 深度优先搜索
- DFS 广度优先搜索
- Dijkstra 最短路径算法
- Prim 最小生成树
- Kruskal 最小生成树

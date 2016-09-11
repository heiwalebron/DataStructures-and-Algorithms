# DataStructures-and-Algorithms
## 1.不同数据结构之间的比较
| 数据结构       | 优点                                 |        缺点            |
| ---------------|--------------------------------------|------------------------|
| 数组           | 插入快,如果知道下标，可以非常快的存取|查找慢，删除慢，大小固定|
|有序数组        |比无序数组查找快                      |删除和插入慢，大小固定 |
|栈              |提供后进先出方式的存取                |存取其他项很慢         |
|队列            |提供后进先出方式的存取                |存取其他项很慢         |
|链表            |插入快，删除快                        |查找慢                 |
|二叉树          |查找、插入、删除都快（如果树保持平衡）|删除算法复杂           |
|红-黑树         |查找、删除、插入都快。述总是平衡的    |算法复杂               |
|2-3-4 树        |查找、删除、插入都快。                |算法复杂               |
|哈希表          |如果关键字已知，则存取速度极快。插入快|删除慢，如果不知道关键字，则存取很慢，对存储空间使用不充分|
|堆              |插入、删除快，对最大数据线项存储很快  |对其他数据项存取很慢    |
|图              |对现实世界建模                        |有些算法慢且复杂        |

综上，数据结构之间的比较是在查找、删除和插入三个功能之间进行，数组普遍存在插入快，但是查找和删除比较慢；

## 2.算法编程题汇总
- 二维数组中的查找

 在一个二维数组中，每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。

```
public class Solution {
    public boolean Find(int [][] array,int target) {
        int len = array.length-1;
        int i = 0;
        while((len >= 0)&& (i < array[0].length)){
            if(array[len][i] > target){
                len--;
            }else if(array[len][i] < target){
                i++;
            }else{
                return true;
            }
        }
        return false;

    }
}
```



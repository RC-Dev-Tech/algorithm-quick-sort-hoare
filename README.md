# ![](https://drive.google.com/uc?id=10INx5_pkhMcYRdx_OO4rXNXxcsvPtBYq) Quick Sort（Hoare partition scheme）<br> 快速排序（霍爾分區方案）
> ##### 理論請自行找，網路上有很多相關的文章，這邊只關注於範例實作的部分.

---

<!--ts-->
## 目錄
* [簡介](#簡介)
* [示意圖](#示意圖)
* [實作範例](#實作範例)
* [參考資料](#參考資料)
<!--te-->

---

## 簡介
快速排序（Quick Sort）是一種常見且高效的排序算法，屬於比較排序的一種。<br>
它的基本概念是選擇一個基準元素（pivot），將數列劃分為兩個子數列，<br>
其中一個子數列中的元素都小於基準元素，另一個子數列中的元素都大於基準元素。<br>
然後對兩個子數列分別遞迴地應用快速排序，直到排序完成。<br>
<br>
Hoare partition scheme 則是快速排序的一種分區方案，其過程如下：<br>
- 選擇數列中間的元素作為基準點（pivot）。
- 初始化兩個指標，一個指向數列的起始位置（low），另一個指向數列的末尾位置（high）。
- 重複以下步驟直到兩個指標相遇：
  - 從左側開始，尋找第一個大於等於基準點的元素。
  - 從右側開始，尋找第一個小於等於基準點的元素。
  - 如果兩個指標尚未相遇，則交換這兩個元素。
- 當兩個指標相遇時，將基準點與這個位置的元素進行交換，這樣基準點左邊的元素都小於等於基準點，右邊的元素都大於等於基準點。
- 遞迴應用快速排序到基準點左右兩個子數列上，直到排序完成。

<br>

其時間複雜度：<br>
- 平均情況下：O(n log n)
- 最壞情況下（當數列已經有序）：O(n^2)
- 最好情況下（當數列元素分布較為均勻）：O(n log n)
<br>
Hoare partition scheme在某些情況下比Lomuto partition scheme的效率更高，因為它在分區過程中避免了不必要的元素交換。<br>
然而，由於Hoare partition scheme的實現較為複雜，並且在某些特定情況下可能導致不均勻的分割，因此在實際應用中需要謹慎考慮使用。

---

## 示意圖:
<img src="https://drive.google.com/uc?id=1JJv1ARTBczJaDoBM2UOY9SmBv7Ups8Jtt" height="70%" width="70%"/>
<img src="https://drive.google.com/uc?id=1BF_4bE_VAByMQZvCP_GqW6mYCzhOdHMjj" height="70%" width="70%"/>

> 圖片來源：[iThome鐵人賽(Frank) - 演算法 快速排序法 Quick Sort](https://ithelp.ithome.com.tw/articles/10278644)

---

## 實作範例:
- [Example](https://github.com/RC-Dev-Tech/algorithm-quick-sort-hoare/blob/main/C%2B%2B/main.cpp) - Hoare Quick Sort (C++)

---

## 參考資料
* [Wiki - Quick Sort](https://zh.wikipedia.org/wiki/%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F) <br>
* [iThome鐵人賽(Frank) - 演算法 快速排序法 Quick Sort](https://ithelp.ithome.com.tw/articles/10278644) <br>

---

<!--ts-->
#### [目錄 ↩](#目錄)
<!--te-->
---

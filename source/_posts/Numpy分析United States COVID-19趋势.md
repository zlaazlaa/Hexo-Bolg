# Numpy分析United States COVID-19趋势

<p style="text-align:right">B20090611马青宇</p>

## 数据抓取

从约翰斯·霍普金斯大学网站上抓取数据[United States - COVID-19 Overview - Johns Hopkins (jhu.edu)](https://coronavirus.jhu.edu/region/united-states)

> 抓取了从疫情开始到现在的全部数据

<figure class="half">
    <img src="C:\Users\zlaa\AppData\Roaming\Typora\typora-user-images\image-20221112152531467.png", width=50% /><img src="C:\Users\zlaa\AppData\Roaming\Typora\typora-user-images\image-20221112152940507.png", width=50% />
</figure>

## 数据整理

使用`json.loads`进行数据整理。

使用`np.poly1d`进行模型的预测。

使用`sklearn.metrics`进行$R^2$的计算。

选取拟合效果最好的结果进行输出。

## 预测结果

```c++
R^2 = 0.64
```

```c++
            47             46              45              44
2.169e-126 x  - 6.09e-123 x  + 1.653e-120 x  + 4.918e-117 x 
               43              42              41              40
 + 2.081e-114 x  - 2.346e-111 x  - 4.398e-108 x  - 2.983e-105 x 
               39             38             37             36
 + 4.552e-103 x  + 3.475e-99 x  + 4.228e-96 x  + 2.377e-93 x 
              35             34             33             32
 - 8.965e-91 x  - 3.657e-87 x  - 4.299e-84 x  - 2.421e-81 x 
              31             30            29             28
 + 9.355e-79 x  + 3.822e-75 x  + 4.46e-72 x  + 2.324e-69 x 
              27             26             25             24
 - 1.397e-66 x  - 4.342e-63 x  - 4.403e-60 x  - 1.264e-57 x 
              23             22             21             20
 + 3.004e-54 x  + 5.078e-51 x  + 2.913e-48 x  - 2.054e-45 x 
              19            18             17             16
 - 5.311e-42 x  - 3.12e-39 x  + 2.844e-36 x  + 5.619e-33 x 
              15             14             13             12
 + 6.985e-31 x  - 5.707e-27 x  - 2.573e-24 x  + 5.999e-21 x 
              11             10             9             8
 + 1.503e-18 x  - 7.482e-15 x  + 6.515e-12 x - 3.098e-09 x
              7             6           5        4         3        2
 + 9.352e-07 x - 0.0001867 x + 0.02461 x - 2.08 x + 105.9 x - 2892 x + 3.42e+04 x - 1.041e+05
```

<figure class="half">
    <img src="C:\Users\zlaa\AppData\Roaming\Typora\typora-user-images\image-20221112153418658.png", width=50%><img src="C:\Users\zlaa\AppData\Roaming\Typora\typora-user-images\image-20221112153427390.png", width=50%> </figure>


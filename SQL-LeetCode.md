```sql
 如何查出第二高的数据记录

题解：去重，和查出为 null的情况。

 解法一： select (select distinct salary  from employee order by salary desc limit 1,1)as SecondHighestSalary   -- 查出的数据作为临时表。

解法二： 
 select (ifnull((select distinct salary  from employee order by salary desc limit 1,1),null))as SecondHighestSalary    -- 添加函数 时间复杂度太高。

 刚创建的 github 仓库
```


# R-learn
## part1 homework answer  
1.统计 `test_command.gtf`行数和字数  
```  
wc -l test_command.gtf > test_command.txt  
wc -c test_command.gtf >> test_command.txt  
cat test_command.txt  
```
2.利用 `grep `等命令尝试筛选并输出示例文件中以` chr_ `起始，并且基因id为`YDL248W `  
```
grep `chr` test_command.gtf | grep 'YDL248'
```  
3.利用  `sed`  等命令将示例文件中的  `chr_ ` 替换为 ` chromosome_ ` 并输出每行的第1，3，4，5列。（无需改动原文件，只输出结果）  
```
sed 's/chr_/chromosome_/g' test_command.gtf | cut -f 1,3,4,5
```
4. 通过 `man` 命令以及更多的资料学习简单的 `awk` 命令，尝试互换示例文件的第2列和第3列，并且对输出结果利用 `sort` 命令依照第4和第5列数字大小排序，将最终结果输出到 `result.gtf` 文件中。
```
awk '{line=$2; $2=$3; $3=line; print}' test_command.gtf | sort -n -k 4,4 -k5,5 > result.gtf
```
5. 更改示例文件的权限，使得文件所有者及所在用户组用户可读、写、执行而其他用户只可读，展示权限修改前后的权限变化。
```
chmod -R 774 cp_floder
```


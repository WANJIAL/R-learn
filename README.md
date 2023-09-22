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

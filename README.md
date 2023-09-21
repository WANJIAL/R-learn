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

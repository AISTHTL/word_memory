<img width="304" height="317" alt="惩罚任务" src="https://github.com/user-attachments/assets/4e291f1d-8a4c-4309-88ce-78912f8854e9" />双击“word_memory.exe”即可运行
该程序适合久坐于电脑前的同志，平时工作可以顺便背点单词，并提示自己起身促进血液循环

使用说明：

在words.xlsx中只需要设置第二列word（问题）和第三列mean（正确答案）
可以设置自己想要记忆的单词

双击“单词记忆.exe”程序
在限定时间内先回答第一个单词的意思
回答正确则继续随机等待5-10分钟，程序会按顺序对下一个单词弹窗提问
回答错误则会出现惩罚提示和倒计时，惩罚和倒计时可在tasks.txt文件中自行设置
格式为“惩罚内容,惩罚时间（秒）”例如“做十个俯卧撑,60”
并且会在下一次的提问中再次问回答错误的单词，直到回答正确为止


config.ini文件为基础参数设置

total_time = 3600           #设置程序运行时间为3600秒即1小时
min_interval = 300          #设置随机提问时间间隔最小值为300秒即5分钟
max_interval = 600         #设置随机提问时间间隔最大值为600秒即10分钟
penalty_time = 15          #设置惩罚默认时间15秒
answer_wait_time = 5    #设置提交问题后等待时间5秒
answer_time_limit = 20  #设置回答问题时间限制20秒
auto_start = true             #设置双击.exe文件后总倒计时自动开始，true为允许自动开始
auto_add_words = true  #设置word.xlsx中的单词背完后是否自行提问新单词，true为允许自行提问

当程序提问到某个单词后，该单词在words.xlsx中会在number字段自动+1，表示该单词已经背了3遍了，time表示最近记忆的时间（运行该功能时请保持.xlsx文件关闭）

总倒计时结束，程序自动关闭

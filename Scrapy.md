## Scrapy 笔记

> ## 创建项目和爬虫
>
> 1.创建项目：`scrapy startproject [爬虫的名字]`
>
> 2.创建爬虫：进入到项目所在的路径，执行命令：`scrapy genspider [爬虫名字][爬虫的域名]`，注意，爬虫名字不能和项目名称一致

follow 为 True，拿到响应后，除了会给回调函数，还会提取响应里面的 url，再进行提取 url 和匹配 rules 规则

follow 为 False，拿到响应后，不对响应进行链接提取和分析


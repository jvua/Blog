## Scrapy 笔记

> ## 创建项目和爬虫
>
> 1.创建项目：`scrapy startproject [爬虫的名字]`
>
> 2.创建爬虫：进入到项目所在的路径，执行命令：`scrapy genspider [爬虫名字][爬虫的域名]`，注意，爬虫名字不能和项目名称一致

follow 为 True，拿到响应后，除了会给回调函数，还会提取响应里面的 url，再进行提取 url 和匹配 rules 规则

follow 为 False，拿到响应后，不对响应进行链接提取和分析

> scrapy startproject [项目名称]
>
> Scrapy genspider 爬虫名字 “域名”
>
> Settings.py 
>
> > ROBOTSTXT_OBEY = False 机器人协议
> >
> > DEFAULT_REQUEST_HEADERS 中添加 ‘User-Agent'

> URI: Uniform Resource Identifier 统一资源标志符
>
> URL: Universal Resource Locator 统一资源定位符
>
> URL 是 URI 的子集
>
> URI 还包括一个子类叫作 URN（Universal Resource Name）统一资源名称。URN 只命名资源而不指定如何定位资源。


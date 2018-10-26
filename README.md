## 需求分析
```
浏览亚马逊网站选购商品时，种类繁多的商品往往让人眼花缭乱，当选择一个商品进入商品页面时，页面上丰富的信息，如销量、库存量、评价信息等，
不能直观的全方位展现商品各个维度的情况。考虑到这个问题，结合当前开放的Product Advertising API，我们设计了一个商品可视化分析平台，
分析用户搜索的某个商品的详细信息，并通过可视化的方式展示出来，使用户对商品有更全面和直观的了解，节约时间，方便决策。
```
## 产品概述
```
该商品可视化分析平台调用亚马逊提供的Product Advertising API中的ItemLookup接口，获取用户搜索的某个商品的全部数据，
通过分析，将商品信息以饼图、折线图、词云等形式进行可视化展示。为了便于分析，目前只支持对书籍的可视化分析。

调用接口获取书籍数据后，通过抓取评论信息，并对所有评论信息进行情感分析和关键词提取，评论摘要提取，可以得到好中差评的分布情况、
评论的情感走向、商品的近期销量、纸质书和电子书的销量、评价的关键词等，最终展现给用户该书籍的图片、评价分布饼图、评价情感走向图、
近期销量折线图、纸质书与电子书销量对比图、评价词云、相关书目等，使用户对该书籍的销售情况有更直观全面的了解，为选购书籍提供决策支持。
```
## 项目主要模块
```
1.自然语言处理模块，包括爬虫获取商品的用户评论信息模块，评论情感分析模块，评论关键词提取模块，评论摘要提取模块。
2.java后台请求各个模块的服务，分析数据
3.前端可视化
```
## 项目路径
```
1.自然语言处理模块
- amazon_flaks
 - flaskr:将爬虫模块，情感分析模块，关键词提取模块封装为resful接口，与java后台进行通信。
 - emotion:情感分析模块
  - emotionanalysis_amazon.py
 - keyword:关键词提取模块
  - keyword.py
 - indexspider:爬虫模块
  - indexspider
   - spiders
    - spider.py
    
2.javaWeb（后台+前端）
- AmazonDemo
 - /src/main/java/com/amazon/web/controller/serachController
 - /src/main/java/com/amazon/web/service/serachService
 - webapp
  - FigBook
   -index.jsp # 搜索栏首页
   -analyser.jsp # 分析页面

3.平台展示示例图片
- imageDemo
```

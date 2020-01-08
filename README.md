# 项目名称：云秘
标题|内容
---|--:
产品名称|云秘
文档所有者|黄汉铭
设计者|黄汉铭
测试者|黄汉铭
发布日期|2019.12

### 产品介绍
“云秘”是帮助学生党或是上班族记录课程和会议的一款产品
本软件是基于录音识别和文本纠错研发的会议记录工具，适用于学生党和上班族对课堂和会议的记录，通过录音识别将录音转化为文本，再通过文本纠错将录音识别的文本错误纠正增加转换的正确率，以此来便利人们对会议和课堂的记录让工作和学习更加简单快捷。

### 背景
现今学生党和上班族的学习和工作压力日渐加大，手动的课堂或者会议的记录不仅十分的耗费精力和时间而且还会出现偏差和错误。目前市面上还没有出现以课堂和会议记录为主要目标的语音转文本的软件，多数语音转文字的软件只是针对短语音或者是作为聊天软件的附属功能，而长语音转文本的软件多数使用在专业领域而且多为收费服务，以此为背景我们的产品可以填补目前市场上的空白。

### 目标
+ 通过使用录音识别来让会议和课堂的记录变得简单方便（前期目标）
+ 通过使用文本纠错来纠正录音转文本中出现的偏差或者错误让录音转出来的文本准确率更加高（前期目标）
+ 添加组群和任务创建功能（后期目标）

## 价值主张设计
### 加值宣言
本产品通过录音识别和文本纠错来简化会议和课堂记录流程，来方便人们工作和学习
+ 录音识别：通过识别录音将语音转化为文本，以此来简化会议和课堂记录流程
+ 文本纠错：通过文本纠错对录音识别转化的文本进行纠错和改正提高录音转化的正确率

### 核心价值与用户痛点
+ 核心价值：将会议或者课堂录音转化为文本形式，供用户查看、使用、编辑
+ 用户痛点：

1.学生课程较多无法每一堂课都可以集中精力做课堂笔记

2.工作会议的内容繁琐复杂无法很详细的把全部记录下来

3.会议和课堂上总是会有开小差的人，需要让他们在会议或课程过后也能够通过其他方式详细了解会议和课程的内容

### 人工智能概率性与用户痛点
+ 录音清晰 背景没有噪音——文本转换正确率十分高
+ 录音清晰 背景有噪音——文本转换正确率降低，文本内会出现非录音内容的字
+ 录音不清晰 背景没有噪音——文本转换正确率较高，但会出现部分不清晰的录音缺失或是有歧义
+ 录音不清晰 背景有噪音——文本转换正确率地，会出现部分不清晰的录音缺失或是有歧义以及会有非录音内容的字出现

### 需求列表与人工智能API加值

API|使用场景|需求列表|核心功能|重要性
---|:--:|:--:|:--:|--:
录音识别|在会议过后小明需要把会议录音手动转化为文本|对录音进行文本转换|完成录音转文本的工作|最重要
文本纠错|小明在把录音转化为文本之后发现有很多语法或是其他的错误|对转换的文本进行纠错|完成对文本内容的纠错|重要

## 原型
### 产品架构图
![产品架构图](https://github.com/NFUNM024/api-/blob/master/%E6%A1%86%E6%9E%B6%E5%9B%BE.png "")
### 交互及界面设计
+ 腾讯云录音识别API：在转换内容的文本内容输出结果处使用
+ 百度文本纠错API：在文本纠错页面输出结果处使用
![录音识别](https://github.com/NFUNM024/api-/blob/master/8.png "录音识别")
![文本纠错](https://github.com/NFUNM024/api-/blob/master/9.png "录音识别")
### 信息设计
![1](https://github.com/NFUNM024/api-/blob/master/1.png)
![2](https://github.com/NFUNM024/api-/blob/master/2.png)
![3](https://github.com/NFUNM024/api-/blob/master/3.png)
![4](https://github.com/NFUNM024/api-/blob/master/4.png)
![5](https://github.com/NFUNM024/api-/blob/master/5.png)
![6](https://github.com/NFUNM024/api-/blob/master/6.png)
![7](https://github.com/NFUNM024/api-/blob/master/7.png)
### 原型文档 
[云秘原型文档](http://nfunm024_admin.gitee.io/prototype/#g=1&p=%E5%B0%81%E9%9D%A2)
[云秘原型文档下载](https://gitee.com/NFUNM024_admin/prototype)
### 口头操作说明
本产品使用了两个API分别是腾讯云录音识别API和百度文本纠错API。主要的功能为通过用户使用APP进行录音生成录音文件或是选择使用本地录音对录音进行录音识别，通过录音识别API将录音转换为文本输出到APP的文本框内再保存到用户的收集储存内或是APP的云端内。辅助功能为选择云端内的文本文件或是本地的文本文件，通过文本纠错API对转换的文本内的病句、口误、停顿进行修改输出一份错误较少的文本文件再保存到用户的收集储存内或是APP的云端内供用户使用。

## API产品使用关键AI或机器学习之API的输出入展示
### 使用水平
1.腾讯录音识别API调用
+ 获取语音识别token
![语音识别token](https://github.com/NFUNM024/api-/blob/master/1%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%ABtoken.png "")
+ 使用token获取taskid
![腾讯录音识别调用](https://github.com/NFUNM024/api-/blob/master/2%E8%85%BE%E8%AE%AF%E5%BD%95%E9%9F%B3%E8%AF%86%E5%88%AB%E8%B0%83%E7%94%A8.png "")
+ 输出taskid


![获得taskid](https://github.com/NFUNM024/api-/blob/master/3%E8%8E%B7%E5%BE%97taskid.png "")
+ 通过taskid调用腾讯录音识别API
![使用taskid调出结果](https://github.com/NFUNM024/api-/blob/master/4%E4%BD%BF%E7%94%A8taskid%E8%B0%83%E5%87%BA%E7%BB%93%E6%9E%9C.png "")
+ 输出转换结果
![最终结果](https://github.com/NFUNM024/api-/blob/master/5%E6%9C%80%E7%BB%88%E7%BB%93%E6%9E%9C.png "")

2.百度文本纠错API

+ 使用代码获取assess_token
![获取assess_token](https://github.com/NFUNM024/api-/blob/master/7%E8%8E%B7%E5%8F%96assess_token.png "")
+ 通过assess_token调用百度文本纠错API并输出结果
![百度文本纠错功能调用] (https://github.com/NFUNM024/api-/blob/master/8%E7%99%BE%E5%BA%A6%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E5%8A%9F%E8%83%BD%E8%B0%83%E7%94%A8.png "")
### 使用比较分析 
+ 录音识别api
#### 价格
+ 百度短语音识别
![百度](https://github.com/NFUNM024/api-/blob/master/%E7%99%BE%E5%BA%A6%E7%9F%AD%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB.png "")
+ 腾讯录音识别

预付费

![预付费](https://github.com/NFUNM024/api-/blob/master/%E8%85%BE%E8%AE%AF%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB.png "")

后付费

![后付费](https://github.com/NFUNM024/api-/blob/master/%E8%85%BE%E8%AE%AF%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB1.png "")
+ 阿里录音识别

预付费

![预付费](https://github.com/NFUNM024/api-/blob/master/%E9%98%BF%E9%87%8C%E9%A2%84%E4%BB%98%E8%B4%B9%E6%96%B9%E5%BC%8F.png "")

后付费

![后付费](https://github.com/NFUNM024/api-/blob/master/%E9%98%BF%E9%87%8C%E5%90%8E%E4%BB%98%E8%B4%B9.jpg "")

#### 输出结果
+ 腾讯录音识别

![腾讯输出](https://github.com/NFUNM024/api-/blob/master/%E8%85%BE%E8%AE%AF%E4%BB%A3%E7%A0%81%E8%BE%93%E5%87%BA.png "")

+ 阿里录音识别

![腾讯输出](https://github.com/NFUNM024/api-/blob/master/%E8%85%BE%E8%AE%AF%E4%BB%A3%E7%A0%81%E8%BE%93%E5%87%BA.png "")

#### 对比
+ 

### 使用后风险报告
### 加分项

# Jokit

> Java toolkit，java工具包，包含了很多实用常用的工具方法。

[TOC]


## 简介
### 最近更新
* 0.7.0
  新增ClassUtils，可扫描（过滤）项目中所有类
  
* 0.8.0
  新增定时器工具（基于quartz）

## 使用
导入[release](https://github.com/i-hujinwen/JUtils/releases)中的jar包


## 详解
> 此处未一一列举，详细内容请在使用中发现

### 日期相关

#### 自动日期抽取

```java
final String str = DateUtils.convertTime("就在10天前特朗普");  // 输出 2020-03-29 00:00:00
final String str2 = DateUtils.convertTime("时间是，2020年3月4日。");  // 输出 2020-03-04 00:00:00
final String str3 = DateUtils.convertTime("你的未来是我的昨天");  // 输出 2020-04-07 00:00:00
final String str4 = DateUtils.convertTime("这是一段废话1996/09/09 23:12:12");  // 输出 1996-09-09 23:12:12
```



### json相关

#### 字符串与对象相互转换

```java
// 字符串转json
final JsonNode jsonNode = JsonUtils.toJsonNode("");
// 字符串转对象
final Object obj = JsonUtils.toObj("", Object.class);
// 对象转字符串
final String objStr = JsonUtils.toString(new Object());
```



### 邮件相关

#### 获取规范化HTML邮件内容



### 随机相关

#### UUID

```java
final String uuid = RandomUtils.uuid();
```



#### 从集合数组中随机选择

```java
final String str = RandomUtils.randomChoice(new HashSet<String>());
final String str2 = RandomUtils.randomChoice(new String[22]);
```





### Url相关

#### 相对路径转绝对路径

```java
final String result = UrlUtils.absUrl("https://www.baidu.com/s?wd=%22%E6%90%9C%E7%B4%A2%22", "/s?wd=%22%E6%90%9C%E7%B4%A2%22&pn=10&oq=%22%E6%90%9C%E7%B4%A2%22&rsv_page=1");
```






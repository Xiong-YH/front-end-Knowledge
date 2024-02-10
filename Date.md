# date

## 表示方式

- RFC 2822

![image-20240210113013148](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240210113013148.png)

- ISO 8601

```js
new Date().toISOString()
//2024-02-10T03:30:45.719Z
```

## 获取信息方法

- getFullYear()：获取年份
- getMonth()：获取月份，0到11
- getDate()：获取当月具体日期，1到31
- getHours()：获取小时
- getMInutes()：获取分钟
- getSeconds()：获取秒钟
- getMilliseconds()：获取毫秒

**获取某周中的周几**

getDay()：从0到6

## 设置信息（设置超范围的数值，会自动校准

- setFullYear(year, [month], [date])

- setMonth(month, [date])

- setDate(date)

- setHours(hour, [min], [sec], [ms])

- setMinutes(min, [sec], [ms])

- setSeconds(sec, [ms])

- setMilliseconds(ms)

- setTime(milliseconds）

  

## date获取时间戳Unix

**Unix时间戳**：整数值，表示自1970年1月1日以来的毫秒数

获取时间戳

- new Date().getTime()
- new Date().valueOf()
- +new Date()
- Date.now()

**Date.parse(str)等同于 new Date(dateString).getTime() 操作；**

​																									


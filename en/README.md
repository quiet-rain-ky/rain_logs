### rain_logs Introduction

This is a neat little logging tool

### Instructions

1. Import and create objects, object initialization

```js
import logObj from "rain_logs";
/**
 * @param isConsole boolean 类型 : 是否打印到控制台, 默认 true
 * @param isConsoleStyle 是否打印彩色日志, 默认值: false (注意: 此设置只在浏览器才能生效)
 */
var rain_log = new logObj(true, false);
rain_log.setIsConsole(true); // 动态设置是否 控制台打印, 默认值: true
rain_log.setIsConsoleStyle(true); // 动态设置是否 显示控制台日志的样式, 一般只在浏览器的控制台中生效, 默认值: false
```

1. Logging at different levels using object methods

```js
/**
 * 自定义日志类型
 * @param rank 日志级别字符, 例: 'INFO', 可为 null
 * @param sty 日志在控制台的样式, 非 PC 浏览器, 不可使用, 可为 null
 * @param str 要打印的日志内容
 */
rain_log.logs("DEBUG", "color: white; background-color: red;", "logs String");

// 你还可以使用内部方法, 进行日志记录
rain_log.INFO("logs String");
rain_log.DEBUG("logs String");
rain_log.ALL("logs String");
rain_log.TRACE("logs String");
rain_log.WARN("logs String");
rain_log.ERROR("logs String");
```
### rain_logs 介绍

这是一个简洁的小型日志工具

### 使用方法

1. 导入并创建对象, 对象初始化

~~~js
import logObj from "rain_logs";
/**
 * @param optionObj 日志初始化参数对象
 */
var rain_log = new logObj({
    isConsole: true, // 是否开启日志打印功能
    isConsoleStyle: false, // 是否开启日志样式功能, 默认: false 不开启, 注意: 非 PC 浏览器此项不可用
    markStr: "mark string", // 是否在打印日志时, 在日志的前面添加  [ 'markStr' ] 标志
});
rain_log.setIsConsole(true); // 动态设置是否 控制台打印, 默认值: true
rain_log.setIsConsoleStyle(true); // 动态设置是否 显示控制台彩色日志标识, 一般只在浏览器的控制台中生效, 默认值: false
rain_log.version_logs("1.0.0", "https://xxx.com", "orange"); // 日志打印, 版本标识
~~~

2. 使用对象的方法,  进行不同级别的日志记录

~~~js
/**
 * 自定义日志类型
 * @param rank 日志级别字符, 例: 'INFO', 可为 null
 * @param str 要打印的日志内容
 */
rain_log.logs("DEBUG", "logs String");

// 你还可以使用内部方法, 进行日志记录
rain_log.INFO("logs String");
rain_log.DEBUG("logs String");
rain_log.ALL("logs String");
rain_log.TRACE("logs String");
rain_log.WARN("logs String");
rain_log.ERROR("logs String");
~~~

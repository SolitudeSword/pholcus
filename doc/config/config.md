# pholcus_pkg/config.ini 配置说明
*所有的默认值设定变量在config/setting.go，值不存在或者不正确时取默认*

[toc]


## 类型配置方式
### 布尔
配置文件的值会区分大小写
*   正确的true
    +   1
    +   t
    +   T
    +   true
    +   TRUE
    +   True
    +   YES
    +   yes
    +   Yes
    +   Y
    +   y
    +   ON
    +   on
    +   On
*   正确的false
    +   0
    +   f
    +   F
    +   false
    +   FALSE
    +   False
    +   NO
    +   no
    +   No
    +   N
    +   n
    +   OFF
    +   off
    +   Off


## 默认节
默认节即前面未归入任何节的部分

### crawlcap

*   正整数
*   默认变量 _crawlcap_
*   蜘蛛池最大容量


### phantomjs
*   字符串
*   默认变量 _phantomjs_
*   phantomjs文件路径

### proxylib
*   字符串
*   默认变量 _proxylib_
*   代理ip文件路径

### spiderdir
*   字符串
*   默认变量 _spiderdir_
*   动态规则目录

### fileoutdir
*   字符串
*   默认变量 _fileoutdir_
*   文件（图片、HTML等）结果的输出目录

### textoutdir
*   字符串
*   默认变量 _textoutdir_
*   excel或csv输出方式下，文本结果的输出目录

### dbname
*   字符串
*   默认变量 _dbname_
*   数据库名称


## log
### cap

*   正整数
*   默认变量 _logcap_
*   日志缓存的容量

### level
*   枚举类型，字符串，不区分大小写  
    代码中会转换为数字保存  
    从上到下依次变大，设定为某一级之后，设定值及之上的级别都会被输出
    *   app
    *   emergency
    *   alert
    *   critical
    *   error
    *   warning
    *   notice
    *   informational
    *   info
    *   debug
*   默认变量 _loglevel_
*   全局日志打印级别（亦是日志文件输出级别）


### consolelevel
*   枚举类型，字符串，同 **_level_**
*   默认变量 _logconsolelevel_
*   日志在控制台的显示级别
*   如果 **_consolelevel_** 大于 **_level_** 则取 **_level_**


### feedbacklevel
*   枚举类型，字符串，同 **_level_**
*   默认变量 _logfeedbacklevel_
*   客户端反馈至服务端的日志级别
*   如果 **_logfeedbacklevel_** 大于 **_level_** 则取 **_level_**

### lineinfo
*   布尔
*   默认变量 _loglineinfo_
*   日志是否打印行信息

### save
*   布尔
*   默认变量 _logsave_
*   是否保存所有日志到本地文件

## mgo
### connstring
*   字符串
*   默认变量 _mgoconnstring_
*   mongodb连接字符串，类似于 _127.0.0.1:27017_

### conncap
*   正整数
*   默认变量 _mgoconncap_
*   mongodb连接池容量

### conngcsecond
*   正整数
*   默认变量 _mgoconngcsecond_
*   mongodb连接池GC时间，单位秒
### wwwscan.js当初为了学习nodejs自己写的一个小脚本，现在有点时间了，重新把它完善了一下。

#### 特性

* 自动识别404页面
* 支持使用正则过滤404页面
* 支持对字典中的条目后缀进行黑/白名单过滤（只扫描html或者不扫描.bak）
* 从字典的指定位置继续扫描
* 指定时间间隔发送请求
* 自动将扫描结果保存到文本文件

#### ToDo

* Haed发包（有需求了再写）

#### 命令参数

```
node wwwscan.js -h
Usage: wwwscan [options]

Options:
  -V, --version               output the version number
  -H, --HostorDomain <host>   domain or host
  -T, --time <number>         the script sleep time
  -D, --dict <string>         the dict you select
  -C, --continueNum [mnmber]  select continue number to scan
  -B, --blacklist <list>      利用黑名单过滤字典中的后缀（应对waf）
  -N, --notfound <string>     404 regx
  -O, --only <string>         利用白名单过滤字典中的后缀（应对waf）
  -h, --help                  output usage information
```

### screenshot.js批量扫描IP段的某些web端口，并截取并保存网页图片

#### 特性

* 指定特定IP段
* 指定自定义端口（如：80-90，8000）
* 可生成markdown预览
* 自定义chrome代理

#### TODO

代理通过命令行指定

#### 命令行参数

```
λ node screenshot.js -h
Usage: screenshot [options]

Options:
  -V, --version             output the version number
  -H, --ip <ip address>     domain or host
  -P, --port <number>       port
  -F, --listfile <file>     host list
  -O, --outfile <filename>  output file name
  -h, --help                output usage information
```
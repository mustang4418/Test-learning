### 多语言前台生成文件功能测试 #1497
https://github.com/ToubroInfo/AOC/issues/1497


---------



http://testfront.leo.com/index.php?s=/Index_registrymobile.html

生成

域名+/index.php?s=/Index_registrymobile.html

使用 POST 方法,参数名 registryfilename =文件名称，langcode=对应的语言 （如果不传则数据库保存的所有语言都生成一遍）

只能使用 POST 请求,而且参数只能是 registryfilename =文件名称，langcode=对应的语言 否则无效.

恢复

域名+/index.php?s=/Index_registrymob.html

使用 POST 方法,参数名 registryfilename =文件名称，langcode=对应的语言 （如果不传则数据库保存的所有语言都回复一遍），isdel=是否删除被替换的文件（1是删除，0不删除，0时恢复时会把要替换的文件备份）

只能使用 POST 请求,而且参数只能是 registryfilename =文件名称，langcode=对应的语言 否则无效.

文件名称有
lang（前台html中的语言包）
langagent（代理的html语言包）
langpack（前台PHP中的语言包）
common（后台html+PHP中的语言包）

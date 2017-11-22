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


---------------------------





//清除一个全局变量 
pm.globals.unset("variable_key");
//清除一个环境变量
pm.environment.unset("variable_key");
//获取一个全局变量
pm.globals.get("variable_key");
//获取一个变量 、该函数在全局变量和活动环境中搜索变量。
pm.variables.get("variable_key");
//获取一个环境变量
pm.environment.get("variable_key");
//检查响应正文是否包含字符串
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("string_you_want_to_search");
});
//将XML正文转换为JSON对象
var jsonObject = xml2Json(responseBody);
//检查响应体是否等于一个字符串
pm.test("Body is correct", function () {
    pm.response.to.have.body("response_body_string");
});
//检查一个JSON值
pm.test("Your test name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.value).to.eql(100);
});
//内容类型是存在的
pm.test("Content-Type is present", function () {
    pm.response.to.have.header("Content-Type");
});
//响应时间小于200ms
pm.test("Response time is less than 200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});
//发送异步请求、该功能既可以作为预先请求，也可以作为测试脚本使用。
pm.sendRequest("https://postman-echo.com/get", function (err, response) {
    console.log(response.json());
});
//设置一个全局变量
pm.globals.set("variable_key", "variable_value");
//清除一个环境变量
pm.environment.set("variable_key", "variable_value");
//状态码是200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
//代码名称包含一个字符串
pm.test("Status code name has string", function () {
    pm.response.to.have.status("Created");
});
//成功的POST请求状态码
pm.test("Successful POST request", function () {
    pm.expect(pm.response.code).to.be.oneOf([201,202]);
});
//对于JSON数据使用TinyValidator
var schema = {
  "items": {
    "type": "boolean"
  }
};

var data1 = [true, false];
var data2 = [true, 123];

pm.test('Schema is valid', function() {
  pm.expect(tv4.validate(data1, schema)).to.be.true;
  pm.expect(tv4.validate(data2, schema)).to.be.true;
});














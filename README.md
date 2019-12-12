# yjs_oasso
以sso方式登陆系统

## 一、使用说明

该模块遵循集团OA的sso标准，通过集团申请和登记后，集团OA系统会回调SsoController，SsoController通过springSecurity的强制登陆方式承认该用的的登陆行为。
该项目采用grails框架开发，项目结构如下：

assets/**					项目前台资产，包括css，js，images等。

conf/**					项目配置文件所在目录，application.yml为应用主配置。

controllers/**				web控制器所在目录，SsoController.groovy为集团OA回调入口。

domain/**	 			数据库映射代码，每一个*.groovy文件映射一张数据库表，这里包括springSecurity所需的4张基本表。

i18n/**	 				国际化翻译文件目录，messages_zh_CN.properties为中文。

init/**					项目启动文件所在目录。

views/**					web模板所在目录，前台页面都通过模板显示。

##二、实现功能

实现集团OA SSO方式登陆的对接，兼容springSecurity框架，可以实现SSO与传统用户密码的双登陆。采用代码可遵循以下步骤：

1、	申请集团SSO登陆，获得appId和key

2、	将以上信息写入SsoController.groovy

3、	将入口链接放入集团OA某个应用中

4、	实现SSO功能

5、	编写功能代码


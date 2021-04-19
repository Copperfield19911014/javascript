# meta标签部分用法及注意点

## 注意点
>meta标签可提供有关页面的元信息，比如针对搜索引擎和更新频度的描述和关键词<br/>
>html中，meta标签没有结束标签，xhtml中必须被正确关闭

## 用法
1. http-equiv属性

http-equiv="X-UA-Compatible"
如果指定了该值，则content属性必须具有值"IE=edge"。用户代理必须忽略此指示。

---

http-equiv="content-security-policy"
它允许页面作者定义当前页的内容策略。内容策略主要指定允许的服务器源和脚本端点，这有助于防止跨站点脚本攻击。

---

http-equiv="content-type"
如果使用这个属性，其值必须是"text/html; charset=utf-8"。注意：该属性只能用于 MIME type 为 text/html 的文档，不能用于MIME类型为XML的文档。

---

http-equiv="default-style"
设置默认 CSS 样式表组的名称。

---

http-equiv="refresh"
如果content只包含一个正整数， 则为重新载入页面的时间间隔（秒）；
如果content包含一个正整数，并且后面跟着字符串 ';url=' 和一个合法的 URL，则是重定向到指定链接的时间间隔(秒)

---

http-equiv="name"
name 和 content 属性可以一起使用，以名-值对的方式给文档提供元数据，其中 name 作为元数据的名称，content 作为元数据的值。

2. content属性

此属性包含http-equiv 或name 属性的值，具体取决于所使用的值。






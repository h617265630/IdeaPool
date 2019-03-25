新建搜索项/筛选项流程

1. 页面里编写dataFunction 给个名字

filterComponents.js

filterDataActions.js

2. filterDataActions.js 的dataFunction 块中写对应的

dataFunction 函数，名字自定， 和1.中的名字一样。

3. apiMain（main.js\) 中rsDimAPI 新建对应方法

4. apiResource.js 的res中写对应url\(vue.resource 注册\)

5. apiurl中也对应的url

6. route 中写对应的url 和controller方法

7. controller里写对应的方法,调用下一步中model里定义的方法

8. model中定义数据库操作，获取对应数据。对应表。


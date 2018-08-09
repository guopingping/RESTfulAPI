RESTful API
=========================================================
```
1、协议
    使用HTTPs协议
2、域名
    尽量将API部署在专用域名之下
        https://api.example.com
    如果确定api很简单，不会有进一步扩展，可以考虑放在主域名下
        https://example.org/api/
3、版本
    将API版本号放入URL
        https://api.example.com/v1/
4、路径
    又称“终点”，表示API的具体网址
    网址中不能有动词，只能有名词，名词往往与数据库的表格名对应，使用复数
5、HTTP动词
    GET(SELETE)
    POST(CREATE)
    PUT(UPDATE)
    PATCH(UPDATE)
    DELETE(DELETE)
6、过滤信息
    提供参数，过滤返回结果
7、状态码
    200 OK：服务器成功返回用户请求的数据
    201 CREATED：用户新建或修改数据成功
    202 Accepted：表示一个请求已经进入后台排队（异步任务）
    204 NO CONTENT：删除数据成功
    400 INVALID REQUEST：请求错误，服务器没有进行新建或修改数据的操作
    401 Unauthorized：请求的格式不可得
    410 Gone：用户请求的资源被永久删除，且不会再得到的
    422 Unprocesable entity：当创建一个对象时，发生一个验证错误
    500 INTERNAL ERROR：服务器发生错误，用户将无法判断发出的请求是否成功
8、错误处理
    {
        error:''
    }
9、返回结果
10、Hypermedia API
    RESTful API最好做到Hypermedia，即返回结果中提供链接，连向其它API方法，使得用户不查文档，也知道下一步应该做什么
    
```
# Node
### koa中如果用户通过Nginx代理来访问怎么知道对方的真实IP
    1.配置nginx中添加如下信息	
        proxy_set_header Host      $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; 

    2.koa中设置app.proxy = true;或者express中app.enable('trust proxy');
    
    3.如果使用原始获取方式可以获取header中相关参数获取如下
        X-Real-IP,X-Forwarded-For
### MongoDB和MySQL的优劣和适用场景
    MongoDB应用场景：日志记录，缓存数据等，一些无需复杂事务的系统
    特性:单文档事务,可用地理位置索引，数据高可靠，运维简单，开发成本低，适用于简单数据存储等
    3大特性：灵活文档模型 + 高可用复制集 + 可扩展分片集群
    MYSQL:复杂事务的场景
### MySQL事务
    原则：事务要么全部执行，要么全部不执行。
    - BEGIN 开始一个事务
    - ROLLBACK 事务回滚
    - COMMIT 事务确认 
### Node远程调试
    node --inspect-brk=0.0.0.0:7878 (ip:port)
    node --inspect=0.0.0.0:7878 (0.0.0.0代表允许所有链接)
    chrome启用inspect调试工具
    chrome-devtools://devtools/bundled/inspector.html?experiments=true&v8only=true&ws=(ws地址) 
### 集群
    启用共享端口的多线程
# JavaScript
### 原型与原型对象
    js中全是对象
    对象分为普通对象和函数对象
    new Function() 创建的对象都是函数对象，其它是普通对象
    函数的对象的prototype属性就是原型对象
    原型对象有一个默认属性constructor，相当于是一个指针指向构造函数
    原型对象相当于实例化的对象赋值给了原型对象所以有构造函数(原型对象是构造函数的一个实例)
    Function.prototype为函数对象，Function没有原型对象
     
### 原型链
    Person.prototype.constructor == Person;
    类的prototype为原型对象，构造函数再类的原型对象里
    person1.__proto__ == Person.prototype;
    对象的__proto__为类的原型对象
    person1.constructor == Person;
    对象的构造函数和类的构造函数相等

    实例与构造函数的原型对象之间
### 如何完美的继承一个原型链
### 事件驱动
### promise
### 闭包，适用场景，好处
### this的指向

# Vue.js
### 实现数据双向绑定
### vuex深入


# React.js
### 抽空简单学习一下

# Others
### 浏览器渲染过程
### 浏览器缓存机制
### 网络请求status相关
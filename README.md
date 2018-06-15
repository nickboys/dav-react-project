# dav-react-project
第一次使用dav+antd 将步骤记录下来

第一步：安装 dva-cli#

通过 npm 安装 dva-cli 并确保版本是 0.8.1 或以上。
$ npm install dva-cli -g
$ dva -v
0.8.1

第二步：创建新应用

安装完 dva-cli 之后，就可以在命令行里访问到 dva 命令。
$ dva new dva-quickstart

然后我们 cd 进入 dva-quickstart 目录，并启动开发服务器：
$ cd dva-quickstart
$ npm start

几秒钟后，你会看到以下输出：
Compiled successfully!

The app is running at:

http://localhost:8000/

Note that the development build is not optimized.
To create a production build, use npm run build.
在浏览器里打开 http://localhost:8000 ，你会看到 dva 的欢迎界面。

第三步：使用 antd

1.安装 antd 和 babel-plugin-import

方法1：通过 npm 安装

$ npm install antd babel-plugin-import --save

方法2：通过 cnpm 安装

$ npm install -g cnpm --registry=https://registry.npm.taobao.org

$ cnpm install antd 
$ cnpm install babel-plugin-import 


3.定义路由

新建 route component routes/Products.js，内容如下：
import React from 'react';

const Products = (props) => (
  
);

export default Products;



4.添加路由信息到路由表，编辑 router.js :

import React from 'react';
import { Router, Route, Switch } from 'dva/router';
import IndexPage from './routes/IndexPage';
import Products from './routes/Products';

function RouterConfig({ history }) {
  return (
    <Router history={history}>
      <Switch>
        <Route path="/products" exact component={Products} />
      </Switch>
    </Router>
  );
}

export default RouterConfig;
然后在浏览器里打开 http://localhost:8000/#/products 

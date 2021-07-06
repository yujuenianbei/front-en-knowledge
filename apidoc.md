# apidoc使用方法

## 安装

yarn add apidoc

配置package.json

"api": "./node_modules/.bin/apidoc -i routes/ -o public/apidoc/"

根目录添加apidoc.json

{
  "name": "node版前台接口文档",
  "version": "0.0.1",
  "description": "前台接口",
  "title": "Node version foreground interface document",
  "url" : "http://localhost:3000/api/index"
}

## 使用

在对应端口上添加注释

/**
 * @api {post} /users/login 用户登录 // users为路由名称
 * @apiDescription 用户登录
 * @apiName login
 * @apiGroup IndexApi
 * @apiParam {string} username 用户名
 * @apiParam {string} password 密码
 * @apiSuccess {json} result
 * @apiSuccessExample {json} Success-Response:
 *  {
 *      "success" : "true",
 *      "result" : {
 *          "username" : "用户名",
 *          "password" : "密码"
 *      }
 *  }
 * @apiSampleRequest http://localhost:3000/api/index/users/login
 * @apiVersion 0.0.1
 */

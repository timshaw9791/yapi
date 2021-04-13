## 二开指南补充
- [原本的二开指南](https://hellosean1025.github.io/yapi/documents/redev.html)
- 注意其中的需要copy config的步骤，并先确认安装mongodb，创建对应的db以及用户
```bash
# 例如mac下用brew安装 [](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)
  508  brew tap mongodb/brew
  509  brew install mongodb-community@4.4
  510  brew install mongodb-community@4.4
  511  brew services start mongodb-community@4.4
  mongo
  > use yapi
  > db.createUser({user:"test1",pwd:"test1",roles:["readWrite","dbAdmin"]})
#既然node比较老，就用n来
sudo n
#切换到v7.6.0
#升级npm到5.10，只要有切换就要升级npm
sudo npm install -g npm@5
  #按照要求删掉
  sudo rm -rf node_modules
  npm --registry https://registry.npm.taobao.org i
  npm run dev
  #访问http://localhost:3000
  #初始密码是ymfe.org

```

## 在vscode中调试服务器代码
- npm run dev中使用了nodemon --inspect.
- 在vscode的debug面板中启动attach program . 即 .vscode/launch.json中的代码块。
- 给后端代码打断点
  
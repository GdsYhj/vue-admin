# vue-admin

# vscode 与 github 连接
1.github 上新建项目
git config --global user.name GdsYhj
git config --global user.email 295570679@qq.com
ssh-keygen -t rsa -C 295570679@qq.com  这里不要输入密码一路回车下去。
cd /Users/honglan/.ssh/
ls -al
vim id_rsa.pub
ssh -T git@github.com

# github
git branch --list  //列表出所有分枝
git branch dev  //创建dev分支
git push  //推送分支
git checkout dev  //切分支

git branch -a //查看所有分支  本地和远程的分支

git checkout -b name  //创建分支并切到对应分支

npm i yarn -g  安装yarn

vue create vue-admin

cd vue-admin

npm run serve

contorl + c 终止终端

cnpm i element-ui -S 安装 elementui
# 完整引入
import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import App from './App.vue';

Vue.use(ElementUI);

new Vue({
  el: '#app',
  render: h => h(App)
});
# 按需引入
首先，安装 babel-plugin-component：
cnpm install babel-plugin-component -D 
然后，将 .babelrc 修改为：
{
  "presets": [["es2015", { "modules": false }]],
  "plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ]
  ]
}
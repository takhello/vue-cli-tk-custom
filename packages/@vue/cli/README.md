# @vue/cli

``` sh
npm install -g @vue/cli
vue create my-project
```

[Full Docs](https://cli.vuejs.org/)

# 在文件 packages/@vue/cli-plugin-eslint/generator/index.js中 对  package.json 进行写入eslint配置相关的操作，字段eslintConfig
# 文件 packages/@vue/cli/lib/Generator.js 负责生成各种默认配置文件
# 在 packages/@vue/cli/lib/Generator.js 的170行调用了 生成器，生成对应启动方法
    ```js
        // rawPlugins
        { '@vue/cli-plugin-babel': {},
            '@vue/cli-plugin-eslint': { config: 'base', lintOn: [ 'save' ] },
            '@vue/cli-service': { 
                projectName: 'vue-test-cli',
                vueVersion: '2',
                useConfigFiles: false,
                cssPreprocessor: undefined,
                plugins: [Circular] 
            } 
        }
    ```

## 安装日志

baiwang@MacBook-Pro-2 vue-cli % npm run testCli

> @ testCli /Users/baiwang/Documents/store/store-git/vue-cli
> node ./packages/@vue/cli/bin/vue.js create vue-test-cli

 WARN  You are using an outdated version of NPM.
there may be unexpected errors during installation.
Please upgrade your NPM version.


Vue CLI v4.5.7
? Target directory /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli already exists. Pick an action: Overwrite

Removing /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli...


Vue CLI v4.5.7
┌─────────────────────────────────────────┐
│                                         │
│   New version available 4.5.7 → 4.5.9   │
│                                         │
└─────────────────────────────────────────┘

? Please pick a preset: Default ([Vue 2] babel, eslint)


Vue CLI v4.5.7
 WARN  You are using an outdated version of NPM.
there may be unexpected errors during installation.
Please upgrade your NPM version.
create 创建项目 /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli.
create CLI安装插件。这可能需要一段时间...
create 开始执行安装命令
install 下载依赖 开始
install 下载依赖 1.3
runCommand 执行安装命令 开始
execa 执行命令 开始
execa 命令
npm
execa 参数
[ 'install',
  '--loglevel',
  'error',
  '@vue/cli-plugin-babel@~4.5.0',
  '@vue/cli-plugin-eslint@~4.5.0',
  '@vue/cli-service@~4.5.0',
  '--save-dev' ]
execa 路径
/Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli
execa 执行命令 2
execa 执行命令 2.2
execa 执行命令 2.3 npm

> fsevents@1.2.13 install /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/watchpack-chokidar2/node_modules/fsevents
> node install.js

  SOLINK_MODULE(target) Release/.node
  CXX(target) Release/obj.target/fse/fsevents.o
  SOLINK_MODULE(target) Release/fse.node

> fsevents@1.2.13 install /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/webpack-dev-server/node_modules/fsevents
> node install.js

  SOLINK_MODULE(target) Release/.node
  CXX(target) Release/obj.target/fse/fsevents.o
  SOLINK_MODULE(target) Release/fse.node

> yorkie@2.0.0 install /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/yorkie
> node bin/install.js

setting up Git hooks
can't find .git directory, skipping Git hooks installation

> core-js@3.8.1 postinstall /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/core-js
> node -e "try{require('./postinstall')}catch(e){}"


> ejs@2.7.4 postinstall /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/ejs
> node ./postinstall.js

+ @vue/cli-plugin-babel@4.5.9
+ @vue/cli-service@4.5.9
+ @vue/cli-plugin-eslint@4.5.9
added 1241 packages from 948 contributors and audited 1241 packages in 163.886s
found 0 vulnerabilities

execa 执行命令 完成
install 下载依赖 完成
create 第一步安装完成
create 调用生成器...
 WARN  You are using an outdated version of NPM.
there may be unexpected errors during installation.
Please upgrade your NPM version.
create 安装额外的依赖关系...
install 下载依赖 开始
install 下载依赖 1.2
runCommand 执行安装命令 开始
execa 执行命令 开始
execa 命令
npm
execa 参数
[ 'install',
  '--loglevel',
  'error',
  'core-js@^3.6.5',
  'vue@^2.6.11' ]
execa 路径
/Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli
execa 执行命令 2
execa 执行命令 2.2
execa 执行命令 2.3 npm

> core-js@3.8.1 postinstall /Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli/node_modules/core-js
> node -e "try{require('./postinstall')}catch(e){}"

+ core-js@3.8.1
+ vue@2.6.12
added 1 package from 1 contributor, updated 1 package and audited 1242 packages in 10.537s
found 0 vulnerabilities

execa 执行命令 完成
install 下载依赖 1.3
runCommand 执行安装命令 开始
execa 执行命令 开始
execa 命令
npm
execa 参数
[ 'install',
  '--loglevel',
  'error',
  '@vue/cli-plugin-babel@~4.5.0',
  '@vue/cli-plugin-eslint@~4.5.0',
  '@vue/cli-service@~4.5.0',
  'babel-eslint@^10.1.0',
  'eslint@^6.7.2',
  'eslint-plugin-vue@^6.2.2',
  'vue-template-compiler@^2.6.11',
  '--save-dev' ]
execa 路径
/Users/baiwang/Documents/store/store-git/vue-cli/vue-test-cli
execa 执行命令 2
execa 执行命令 2.2
execa 执行命令 2.3 npm
+ eslint-plugin-vue@6.2.2
+ @vue/cli-plugin-babel@4.5.9
+ vue-template-compiler@2.6.12
+ @vue/cli-plugin-eslint@4.5.9
+ babel-eslint@10.1.0
+ @vue/cli-service@4.5.9
+ eslint@6.8.0
added 52 packages from 36 contributors, updated 3 packages and audited 1294 packages in 181.37s
found 0 vulnerabilities

execa 执行命令 完成
install 下载依赖 完成
create 钩子执行完成...
create 生成 README.md...
create 成功创建项目：vue-test-cli.
create 开始使用以下命令: 

 $ cd vue-test-cli
 $ npm run serve
baiwang@MacBook-Pro-2 vue-cli % 
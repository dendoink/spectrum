### 项目依赖安装
* [RethinkDB](https://rethinkdb.com/docs): Data storage
* [Redis](https://redis.js.org/): Background jobs and caching
* [GraphQL](https://graphql.org/graphql-js/): API, powered by the entire Apollo toolchain
* [Flowtype](https://flow.org/en/docs/getting-started/): Type-safe JavaScript
* [PassportJS](http://www.passportjs.org/): Authentication
* [React](https://reactjs.org/docs/getting-started.html): Frontend React app

To have launchd start rethinkdb now and restart at login:
```
brew services start rethinkdb
```

Or, if you don't want/need a background service you can just run:
```
rethinkdb
```

type below:
``` 
brew update
brew install redis
```

To have launchd start redis now and restart at login:

``` 
brew services start redis
```

to stop it, just run:

``` 
brew services stop redis
```

Or, if you don't want/need a background service you can just run:

``` 
redis-server /usr/local/etc/redis.conf
```

Test if Redis server is running.

``` 
redis-cli ping
```

If it replies “PONG”, then it’s good to go!

Location of Redis configuration file.

``` 
/usr/local/etc/redis.conf
```

Uninstall Redis and its files.

``` 
brew uninstall redis
rm ~/Library/LaunchAgents/homebrew.mxcl.redis.plist
```

To have launchd start redis now and restart at login:

```
brew services start redis
```

Or, if you don't want/need a background service you can just run:

```
redis-server /usr/local/etc/redis.conf
```

### 常用 package 
推荐:
- [web-vitals](https://github.com/GoogleChrome/web-vitals#readme)
  [页面加载性能之 Web Vitals](https://juejin.cn/post/6856768621138919432)
- [classnames](https://www.npmjs.com/package/classnames)
- [styled components](https://styled-components.com/docs/api)
  [How to use media queries with styled components](https://jsramblings.com/how-to-use-media-queries-with-styled-components/)

使用中:
- [react-loadable](https://github.com/jamiebuilds/react-loadable#readme)
- [recompose README.md](https://github.com/acdlite/recompose)
- [graphql](https://github.com/graphql/graphql-js)
- [Raven](https://github.com/getsentry/sentry-javascript)
  Sentry is Open-source error tracking that helps developers to monitor, fix crashes in real time. Don't forget about boosting the efficiency, improving user experience. Sentry has support for JavaScript, React, Node, Python, PHP, Ruby, Java and other programming languages.

### 探究问题

- 路由管理
- 全局状态管理
- request 封装
- 类型
- react hooks + redux 使用
- redux devtools
- vscode lint 配置
- ts 常用配置

### best practice

[Redux有哪些最佳实践?](https://www.zhihu.com/question/47995437)
[redux 三重境](https://juejin.cn/post/6844903475516588040)
[React-Redux——提供可预测化的状态管理](https://www.jianshu.com/p/ba4a9fbd2971)
[Redux essentials](https://redux.js.org/tutorials/essentials/part-1-overview-concepts)
[redux vs react context which one should you choose](https://dev.to/ibrahima92/redux-vs-react-context-which-one-should-you-choose-2hhh#:~:text=Redux%20is%20such%20a%20boilerplate,not%20increase%20your%20bundle%20size.)
[React Hooks 最佳实践](https://juejin.cn/post/6844904165500518414)

### redux 替代方案:

[React Hooks vs. Redux: Do Hooks and Context replace Redux?](https://blog.logrocket.com/use-hooks-and-context-not-react-and-redux/)
- [lifting-state-up](https://reactjs.org/docs/lifting-state-up.html)

One way to solve this is to extract the shared state from the components, and put it into a centralized location outside the component tree. With this, our component tree becomes a big "view", and any component can access the state or trigger actions, no matter where they are in the tree!

### React hooks
* [RethinkDB](https://rethinkdb.com/docs): Data storage
* [Redis](https://redis.js.org/): Background jobs and caching
* [GraphQL](https://graphql.org/graphql-js/): API, powered by the entire Apollo toolchain
* [Flowtype](https://flow.org/en/docs/getting-started/): Type-safe JavaScript
* [PassportJS](http://www.passportjs.org/): Authentication
* [React](https://reactjs.org/docs/getting-started.html): Frontend React app

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

### Redux best practice

[Redux有哪些最佳实践?](https://www.zhihu.com/question/47995437)
[redux 三重境](https://juejin.cn/post/6844903475516588040)
[React-Redux——提供可预测化的状态管理](https://www.jianshu.com/p/ba4a9fbd2971)
[Redux essentials](https://redux.js.org/tutorials/essentials/part-1-overview-concepts)

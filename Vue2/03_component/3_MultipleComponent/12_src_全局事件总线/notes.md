TODO:
1. eventBus的BUG很多，Vue3去除了

    这个有大bug，看似巧妙，绑定事件的组件同时使用多次，注册的事件名都一样，最后一个都覆盖了前面都了]
2. 虽然但是，vue官方并不推荐事件总线，$on $off在vue3已经被删除vue
3. 可以不用安装，Vue中的每个组件实例，自身都都有$root，相当于这里安装的$bus，都是指向vm的
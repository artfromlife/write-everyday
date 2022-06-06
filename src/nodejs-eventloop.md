# 什么是 node 事件循环

事件循环是 Node.js 能实现非阻塞IO 的基石 —— 尽管JS是单线程的 —— 通过将操作移交给操作系统内核

现代处理器大多是多线程的，能在背后处理并行操作。 当这些操作完成之后， 内核会通知 Node.js, 然后合适的回调函数会被添加到

poll queue 最终回调被执行

# 解释事件循环

当 Node.js 启动时，它初始化 event loop , 处理输入脚本,这些脚本可能会产生异步的API调用，定时器调用，或者是调用

process.nextTick, 然后开始处理事件循环 （drop into the REPL ? )

timers -> pending callbacks -> idle,prepare -> poll -> check -> close callbacks -> timers

when poll , incoming connections , data ,etc

每个过程我们在 Node.js 中称为 相位 , 每一个相位都有一个 队列 （FIFO) 装着待执行的 callbacks, 每一个相位都是不同的

会执行队列中的回调（全部执行或者达到回调的上限） 一个相位 一个相位的循环



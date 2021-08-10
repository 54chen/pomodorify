# 中文介绍--54chen
番茄工作法是简单易行的时间管理方法。
使用番茄工作法，选择一个待完成的任务，将番茄时间设为25分钟，专注工作，中途不允许做任何与该任务无关的事，直到番茄时钟响起，然后进行短暂休息一下（5分钟就行），然后再开始下一个番茄。每4个番茄时段多休息一会儿。
番茄工作法极大地提高了工作的效率，还会有意想不到的成就感。

# 相比原版的改动
1. 去掉spotify，声破天在大陆是没办法注册的，vpn都不太行得通
2. 添加工作内容
3. 完事后自动提交github
4. 改成强提示，原来的提示不太给力
依然只支持Mac

# 咋用？
先fork到你自己的github账号下，再按如下操作：

```
 git clone git@github.com:{your ID}/pomodorify.git
 cd pomodorify
 sh pomodify.sh 完成100行代码
```

然后你的gihub首页会得到满满一屏的时间线，在这个库中可以看到所有的timeslot (全部记录在git log里了).

```
commit 93c1b9106cb364e39ea0c387c0261cd7834b9190 (HEAD -> master, origin/master, origin/HEAD)
Author: 54chen <czhttp@gmail.com>
Date:   Thu Jun 24 13:22:34 2021 +0800

    Congrats! 13:22 - 13:22 Done! hello
```

# pomodorify
You can use this script to run a simple pomodoro timer that plays music from Spotify while you work from the command line on Mac. 

![Screenshot](https://github.com/ykumards/pomodify/blob/master/pomodify.png)

### Prereqs
* Spotify desktop app (obviously)
* Macvim is used as the default editor, you can use anything else (I've also tested it with sublime)

### Installing
* Clone this repo
* Change the permissions for `pomodify.sh` and `spotify` using `chmod 700`
* Change the logger file path (or comment out all lines related to logging)
* Open Spotify app
* Change the Spotify playlist URI in `pomodify.sh` file. The default is a [coding playlist](https://open.spotify.com/user/125937873/playlist/5SgJR30RfzR5hO21TsQhBp) that I love.
* Run the script using `./pomodify.sh`. You could also add an alias to the `.bash_profile`.

### How it works
1. You can point the script to any Spotify playlist of your choice
2. The music plays when you work (default 25 minute work sessions)
3. The music pauses for 5 mins during the break time 
4. A logger file opens up during the break time, you can type anything you like here
5. The process repeats until you hit Ctrl + C

### Why does this logger thingy popup during breaks?
You can disable this by commenting out the appropriate lines if you'd like, but the main idea was to keep a log of the task that was done, or copying some nagging thoughts onto the dump file, or anything else you want.

### Default Editor
I've used MacVim as the default editor here coz vim is lightweight and is configurable (like, you can open it in such a way that the cursor is always at the end)

### Credits
- The inspiration for this was `christiangenco`'s  comment on [this](https://news.ycombinator.com/item?id=12585670) HN thread.
- The credit for spotify cli integration ENTIRELY goes to `@hnarayanan` and the other contributors of [shpotify](https://github.com/hnarayanan/shpotify).

### License
Meh.



 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

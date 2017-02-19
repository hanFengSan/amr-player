amr-player
使用js来播放amr语音文件, 相对原库来说, 改进了一些非常难用的地方, 并加入了语音时长计算

play remote amr format audio with JavaScript  

fork from https://github.com/alex374/amr-player

## usage
```
// html
<script src="xxx/amrnb.js"></script>
<script src="xxx/amrplayer.js"></script>

// js
var player = new AmrPlayer(amr.url); // after new, AmrPlayer will fetch amr file.
player.then(function () { // the then()'s callback will be executed after fetching file completed
    var duration = player.duration; // can get voice's duration 
    player.play(); // play immediately
    player.endedWith(function () {
        player.pause(); // pause when ending, if not do this, will loop
    });
});

```

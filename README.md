## Using the Player

Add the following script on your HTML:
```html
<head>
  <script src="https://s2.cdn.tv.br/plugins/cdntv-player/cdntv-player.js"></script>
</head>
```
Now, create the player:
```html
<body>
  <div id="player"></div>
  <script>
    var myPlayer = new CdntvPlayer({
        "domain": "example.com.br",
        "user": "user",
        "password": "pwd",
        "playerElement": "player",
    });
    myPlayer.init();
  </script>
</body>
```

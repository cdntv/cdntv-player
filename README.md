# CDNTV Player Plugin

A javascript plugin that was built to help CDNTV customers to display his own channel, provided by CDNTV Media Streaming Engine (like in the other media players developed by CDNTV team), making possible to add it to **any** website that supports javascript.

**Notice:** this plugin is just an additional option developed to help CDNTV customers needs. The other media players developed by CDNTV Team (CDNTV Player Web, CDNTV Player Android, CDNTV Player iOS and CDNTV Player for Set-Top Boxes) will keep receiving periodic updates, as it has been currently.

## Usage

Add the following script on your HTML page head:
```html
<head>
  <script src="https://s2.cdn.tv.br/plugins/cdntv-player/cdntv-player.js"></script>
</head>
```

Inside the body of this page, add the element where the player will stay:
```html
<body>
  <div id="player"></div>
</body>
```

Now, create the CDNTV Player plugin with the desired parameters:
```html
<script>
  var myPlayer = new CdntvPlayer({
      "domain": "example.com.br", //required
      "user": "user", //required
      "password": "pwd", //required
      "playerElement": "player", //required
  
      "protocol": "https", //optional
      "height": 360, //optional
      "width": 640, //optional
      "mute": false, //optional
      "channelGid": "o1ch11" //optional
  });
  myPlayer.init();
</script>
```

## Plugin parameters

Option | Type | Default | Description
------ | ---- | ------- | -----------
domain | string | **required** | Domain name of the CDNTV Media Streaming Engine Edge. Same domain of your CDNTV Player Web
user | string | **required** | User to access the CDNTV Media Streaming Engine
password | string | **required** | Password, corresponding to user previous configured, to access the CDNTV Media Streaming Engine
playerElement | string | **required** | Name of the DOM element id created to display the CDNTV Player
channelGid | string | "o1ch11" | Global identifier of the channel that you want to display on player. You can get this gid on your CDNTV MSE Manager, on channel data.
protocol | string | "https" | Protocol to access the domain given. It will rarely be different from default, but could be "http" in less common cases.
height | integer | 360 | Height of player element body.
width | integer | 640 | Width of player element body.
mute | boolean | false | COnfigure if the player will start muted or not.

## Example running on a wordpress website

[CDNTV Player Plugin Example](http://cdn.tv.br/cdntv-player).

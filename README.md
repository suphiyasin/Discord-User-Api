
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/suphiyasin/Discord-User-API&count_bg=%23C83D3D&title_bg=%23057386&icon=&icon_color=%23BA0808&title=View&edge_flat=false)](https://github.com/suphiyasin/Discord-User-API)


<br />
<p align="center">
<a href="https://github.com/suphiyasin/Discord-User-API/">
<img src="https://www.drupal.org/files/project-images/discord_logo_0.png" alt="Logo" width="800" height="270" />
</a>

<h3 align="center">Dıscord User API V1.0.0</h3>

<p align="center">
    An API that does the user's work.
    <br>
    <a href="https://github.com/suphiyasin/Discord-User-API/issues">Feedback</a>
    <br>
    <a href="https://github.com/suphiyasin/Discord-User-API/blob/main/README-TR.md" style="font-size:24px">Türkçe</a>
</p>

# Firstly
Get CloudFlare cookie from discord.com (For 'im not a robot')
Than use login functions and get token .
First : 
``` 
echo $use->login("mailAdress", "password");
``` 
and copy the result
```
$use->auth = 'PASTE HERE';
``` 
we no longer need to log in on every functions
but if you don't want to write auth code, you have to write login function

# Examples 

### Server
1- Create Channel

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->createServer("My New Server");
```
2-Delete Channel

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
//get server link from any channel
$use->deleteServer("https://discord.com/channels/988562948479910011/988562949226516504");
```
3- Send Message To Servers

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendServer("YOUR MESSAGE", "[LINK OF THE CHANNEL YOU SENT THE MESSAGE]");
```
4- Change Owner

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changeOwner("SERVER LINK", "NEW ADMIN DM LINK (EXPL => https://discord.com/channels/XXXX/XXXX )");
```

5- Join Server
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->joinServer("DISCORD TAG EXMPL => valorant , github ");
//not url
```

### User
1- Change Statu 
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
//invisible, dnd, idle, online
$use->setStatu("online");
```

2-Public Statu
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->PubStatu("Yo Bro Whatzup", "👍");
```

3- Username Change
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changeUsername("NEW USERNAME", "discordPassword");
```

4- Password Change
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changePassword("OLD PASS", "NEW PASS");
```

### Message
1- Send Message To Servers

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendServer("YOUR MESSAGE", "[LINK OF THE CHANNEL YOU SENT THE MESSAGE]");
```

2- Send Message To DM
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendMessage("YOUR MESSAGE", "DM LINK", "RECEIVER USERNAME");
```

3- Show Messages 
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->messages("DM LINK");
```

### Other
1- Get User Info (Profile Pic, UserID)
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->getUserInfo("HER DM LINK", "HER USERNAME");
```

2-Login
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->login("MailAdress", "Password");
//if you are using login function you don't need to specify auth
$use->getUserInfo("HER DM LINK", "HER USERNAME");
//but every time 'functions' logs in, discord says reset password
``` 


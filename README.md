# Discord User API
An API that does the user's work

# Firstly
Get CloudFlare cookie from discord.(For 'im not a robot')
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

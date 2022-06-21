[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/suphiyasin/Discord-User-API&count_bg=%23C83D3D&title_bg=%23057386&icon=&icon_color=%23BA0808&title=View&edge_flat=false)](https://github.com/suphiyasin/Discord-User-API)


<br />
<p align="center">
<a href="https://github.com/suphiyasin/Discord-User-API/">
<img src="https://www.drupal.org/files/project-images/discord_logo_0.png" alt="Logo" width="800" height="270" />
</a>

<h3 align="center">Dıscord User API V1.0.0</h3>

<p align="center">
  Kullanıcıların işini yapan bir API
    <br>
    <a href="https://github.com/suphiyasin/Discord-User-API/issues">Feedback</a>
    <br>
    <a href="https://github.com/suphiyasin/Discord-User-API/blob/main/README-TR.md" style="font-size:24px">English</a>
</p>

# İlk Önce
Discord'tan cookie alın . Lutfen öğeyi incele > network ve gelen xhr verilerinden alınız. Cookie alan eklentiler eksik cookie verebiliyor.
Ve ardından login fonksiyonunu kullanın gelen tokeni bir yere kayıt edin
İlk başta bunu çalıştırın : 
``` 
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
echo $use->login("mailAdress", "password");
``` 
ve gelen sonucu kopyalayınız
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'BURAYA YAPIŞTIR';
//fonksiyonlar...
``` 
artık her fonksiyonda giriş yapmasına gerek yok.
ama isteyenler auth kodunu yazmadan login fonksiyonunu kullansın.

# Örnekler 

### Sunucu
1- Sunucu Oluştur

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->createServer("My New Server");
```
2-Sunucu Sil

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
//get server link from any channel
$use->deleteServer("https://discord.com/channels/988562948479910011/988562949226516504");
```
3-Sunucuya Mesaj gönder

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendServer("YOUR MESSAGE", "[LINK OF THE CHANNEL YOU SENT THE MESSAGE]");
```
4- Sahip aktar

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changeOwner("SERVER LINK", "NEW ADMIN DM LINK (EXPL => https://discord.com/channels/XXXX/XXXX )");
```

5- Sunucuya Katıl
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->joinServer("DISCORD TAG ORNK => valorant , github, elraenn ");
//not url
```

### User
1- Durumu Değiştir.
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
//invisible, dnd, idle, online
$use->setStatu("online");
```

2-Herkese açık durum
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->PubStatu("Yo Bro Whatzup", "👍");
```

3- Username Değiştir
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changeUsername("NEW USERNAME", "discordPassword");
```

4- Şifre Değiştir
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->changePassword("OLD PASS", "NEW PASS");
```

### Message
1- Sunucuya Mesaj gönder

```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendServer("YOUR MESSAGE", "[LINK OF THE CHANNEL YOU SENT THE MESSAGE]");
```

2- DM'e Mesaj Gönder
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->sendMessage("Mesajınız", "Mesaj atıcağınız yerin lınki", "Mesaj atıcağınız kişinin adı");
```

3- Show Messages 
```
$use = new dc();
$use->cookie = 'CLOUDFLARED DISCORD COOKIE';
$use->auth = 'Auth Code';
$use->messages("DM LINK");
```

### Diğer
1- User Info Al (Profile Pic, UserID)
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
//eğer login kullanıyorsan auth belirtmenize gerek yok
$use->getUserInfo("HER DM LINK", "HER USERNAME");
//ama her fonksiyon da giriş yapıcağı için discord şifre değiştir diyor.
``` 


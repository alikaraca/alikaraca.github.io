---
layout: post
title: "Aircrack-ng Kurulumu ve Kullanımı"
date: 2017-07-10
excerpt: "Aircrack-ng"
tags: [aircrack-ng]
comments: true
---
Merhaba arkadaşlar bugün aircrack-ng konusuna değineceğim.İlk olarak; 

## Aircrack-ng nedir?

Aircrack-ng, algılayıcı, paket sezici, 802.11 telsiz LAN için WEP ve WPA/WPA2-PSK
çözücü ve analiz aracından oluşan ağ yazılım takımıdır.802.11a, 802.11b ve 802.11g trafiği
sezebilen bir araçtır.Yani kısacası Wireless Hacking Tools olarak adlandırabiliriz.

## Aircrack-ng İle Neler Yapabiliriz?

-Ağ trafiğini sezebiliriz.

-Dinlediğimiz ağdan paket yakalayabiliriz.

-Modeme bağlı olan bir aracın modeme bağlanmasını engelleyebiliriz.

-WEP ve WPA şifre kırabiliriz.


## Aircrack-ng Kurulumu Nasıl Yapılır?

Bu tür araçların Linux işletim sisteminde kullanılması daha sağlıklı oluyor.Bu yüzden bende Linux'un Ubuntu dağıtımını kullandım.
Kurulumu ve kullanımını bu işletim sistemi üzerinden anlatacağım.Şunu da belirteyim Kali Linux'ta da bu işlemleri yapabilirsiniz.
İlk olarak kurulumu anlatayım.
Bu aracın kurulumu ve kullanımı terminal üzerinden yapacağız.Terminali açalım;
Aracı yüklemek için aşağıdaki kod satırını yazalım.
{% highlight html %}
sudo apt-get install aircrack-ng
{% endhighlight %}
Yükleme tamamlandıktan sonra terminalden devam edeceğiz.
Aracı kullanmak için root yetkisi almamız lazım.
{% highlight html %}
sudo su
{% endhighlight %}yazalım ve ardından kullanıcı şifremizi isteyecek.Kullanıcı şifremizi girdikten sonra root olarak devam edeceğiz.
Şimdi wireless kartımızı öğrenmeliyiz.Bunun için;
{% highlight html %}
ifconfig
{% endhighlight %}komutunu girelim.
<figure>
    <a href="/assets/img/ifconfig.png"><img                                           
    src="/assets/img/ifconfig.png"></a>
</figure>
Wireless kartının listelenmesi lazım benim wireless kartım wlp3s0 ama sizin ki wlan0 olabilir.Komuları ona göre girmelisiniz.
Wireless kartımızı öğrendiğimize göre şimdi wireless kartımızın hangi monitörde çalıştığını görmeliyiz.
Onun içinde;
{% highlight html %}
airmon-ng start wlp3s0
{% endhighlight %}
komutunu yazıyoruz.Dediğim gibi sizin wireless kartınız wlan0 ise onu kullanacaksınız.
<figure>
    <a href="/assets/img/mon.png"><img                                           
    src="/assets/img/mon.png"></a>
</figure>
wlp3s0 ın karşısında yazar hangi monitör modunda çalıştığı ve genelde mon0 da çalışır.Ama benim ki mon4 te sizinde hangisi ise devamında yazdığımız komutlarda ona göre kullanın.
Şimdi de çevremizdeki ağları listeleyelim.
{% highlight html %}
airodump-ng mon0 
{% endhighlight %}
komutunu yazıyoruz.Ve çevremizdeki ağları listeliyoruz.
<figure>
    <a href="/assets/img/ağ listele.png"><img                                           
    src="/assets/img/ağ listele.png"></a>
</figure>
Ağları listeledik şimdi CTRL+C yaparak wireless aramasını durduruyoruz.Şimdi bir hedef seçelim.Ben dördüncü ağı seçtim.Yani kendi ağımı burada kendi ağımı seçmemin nedeni ise konunun genel hatlarını daha kolay ve daha anlaşılır olarak anlatabilmektir.Şimdi seçtiğimiz ağı dinleyeceğiz.Bunun için aşağıdaki komutu yazacağız.
{% highlight html %}
airodump-ng -w "wifiadı" -c "Yayın Yaptığı Kanal" –bssid "Mac adresi" mon0
{% endhighlight %}
Örnek Kullanım
{% highlight html %}
airodump-ng -w TTNET-Airties -c 11 –bssid 18:28:61:F9:5C:8D mon0
{% endhighlight %}
<figure>
    <a href="/assets/img/ağ liste2.png"><img                                           
    src="/assets/img/ağ liste2.png"></a>
</figure>
Şimdi ağı dinlemeye aldık.Gördüğünüz gibi 4 tane station adresimiz var.Bunlar ağımızı bağlı bulunan telefon,bilgisayar vb. aletlerim mac adresleridir.
Ağın şifresini çözebilmemiz için bir paket yakalamamız lazım.Bunun içinde ağda bir hareketlilik olması gereklidir.O yüzden seçtiğimiz bir bilgisayar ya da telefonun ağ ile bağlantısını bir süre kesip otomatik bağlanmasını sağlamalıyız.Başka bir terminal açarak aşağıdaki kod satırını yazmalıyız.Tabi ki önce root olmamız gerekmektedir.
{% highlight html %}
aireplay-ng -0 0 -a "ağın mac adresi" -c "hedef mac adresi" –ignore-negative-one mon0
{% endhighlight %}
Örnek Kullanım
{% highlight html %}
aireplay-ng -0 0 -a 18:28:61:F9:5C:8D -c 20:68:9D:F8:8D:62 –ignore-negative-one mon0
{% endhighlight %}
<figure>
    <a href="/assets/img/bağlantı saldırısı.png"><img                                           
    src="/assets/img/bağlantı saldırısı.png"></a>
</figure>
Bu şekilde hedefe saldırı uygulayarak bağlantısını kestik.CTRL+C yaparak saldırıyı sonlandırıyoruz ve hedef ağa tekrar otomatik bağlanıyor.Böylece biz de paket yakalamış oluyoruz.Yakaladığımız paket wifiadı ile ile kaydolacaktır.Hatırlarsanız yukarıda TTNET-Airties yapmıştık.Yani dosyamız TTNET-Airties.cap olarak kaydedilmiş oldu.Şimdi sona doğru geldik aşağıda yazdığımız komut ile şifreyi çözebilirsek çözeceğiz.
{% highlight html %}
aircrack-ng -w "wordlist" "paket yakaladığımız dosya"
{% endhighlight %}
Örnek Kullanım
{% highlight html %}
aircrack-ng -w /home/ali/Masaüstü/pass.txt TTNET-Airties.cap
{% endhighlight %}
pass.txt:Bu benim oluşturduğum wordlisttir.Sizde bazı wordlist programlarını kullanarak wordlist oluşturabilirsiniz.
TTNET-Airties.cap:Bu da paketlerimizi tutan dosyamız.
<figure>
    <a href="/assets/img/şifre bulma.png"><img                                           
    src="/assets/img/şifre bulma.png"></a>
</figure>
ve sonuç eğer şifre wordlistinizde var ise şifreyi buluyor.
Bu yazımda bu kadar arkadaşlar diğer yazımda görüşmek üzere.
Video anlatımı: 


<iframe width="560" height="315" src="//www.youtube.com/watch?v=n2TAiHvsvr0" frameborder="0"> </iframe>

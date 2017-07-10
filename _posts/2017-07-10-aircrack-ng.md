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
sezebilen bir araçtır.Yani kısacası Wireless Hacking Tools olarak adlandırabiliriz.Aircrack-ng nin kurulumuna geçelim.
Bu tür araçların Linux işletim sistemlerinde kullanılması daha sağlıklı oluyor.Bu yüzden bende Linux'un Ubuntu dağıtımını kullandım.
Kurulumu ve kullanımını bu işletim sistemi üzerinden anlatacağım.İlk olarak kurulumu anlatayım.

## Aircrack-ng Kurulumu Nasıl Yapılır?

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



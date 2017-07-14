---
layout: post
title: "Android ToggleButton ve Switch Kullanimi"
date: 2017-07-14
excerpt: "ToggleButton ve Switch"
tags: [togglebutton,switch,android]
comments: true
---
# Android Studio ToggleButton ve Switch Kullanımı

Arkadaşlar bugün sizlere ToggleButton ve Switch kullanımını anlatacağım ve bunlarla ilgili küçük örnekler göstereceğim.

## ToggleButton Kullanımı

On|Off durumuna göre çalışan bir butondur.Bundan dolayı iki farklı attribute'a sahiptir.Bunlar textOn ve textOff dur.Ayrıca TextView'den türetildiği 
için text özelliği almasına rağmen bunlar textOn ve textOff yüzünden kullanılamamaktadır.Şimdi bir örnek yapacağız.Bu örneğimizde togglebutonun durumuna
göre arka plan rengini kırmızı veya siyah yapacaktır.

activity_main.xml
<script src="https://gist.github.com/alikaraca/c810d711d06e60bfbfdb1f20b3a1dd8f.js"></script>

MainActivity.java

<script src="https://gist.github.com/alikaraca/9462258e6fde13afc38edbbe66eb6eef.js"></script>

## Switch Kullanımı

ToggleButtonun özel bir şeklidir.Bu kontrol (setOnCheckedChangeListener()) fonksiyonu ile kullanılır.Bu fonksiyonda CompoundButton.OnCheckedChangeListener isimli bir interface türündeki nesneyi parametre alır.Bu interface kontrolün durumu değiştiğinde onCheckedChange() isimli callback fonksiyonu tetiklemektedir.Şimdi bunu örnekleyelim.Bu örneğimizde switch durumu değiştiğinde TextView deki yazımız değişecektir.

activity_main.xml

<script src="https://gist.github.com/alikaraca/93c022b51a866ce89cbb488553d5cbf0.js"></script>

MainActiviy.java

<script src="https://gist.github.com/alikaraca/4da41245ebc6ef4a5c552de7c8be239f.js"></script>

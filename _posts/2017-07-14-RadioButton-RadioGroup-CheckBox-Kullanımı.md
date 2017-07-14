---
layout: post
title: "Android'de RadioButton, RadioGroup ve CheckBox Kullanımı"
date: 2017-07-14
excerpt: "RadioButton,RadioGroup ve CheckBox Kullanımı"
tags: [radiobutton,radiogroup,checkbox,android]
comments: true
---
# RadioButton,RadioGroup,CheckBox

Bu nesneler kullanıcıya seçenek sunmak için kullanılır.Aynı anda birden fazla seçenek yapılıp yapılmamasına göre farklılaşır.
İhtiyaçlarımız dahilinde birden çok seçim yapılmak isteniyorsa **_checkbox_** tek bir seçim yapılmak isteniyorsa **_radiobutton_**
kullanırız.RadioButtonların birinin seçilmesini istiyorsak RadioButtonGroup nesnesi kullanılır eğer kullanmazsak checkbox'tan farkı kalmaz.

## CheckBox Örneği

Bu örneğimizde edittextimize girdiğimiz sayı kadar checkbox nesnesini buton yardımı ile oluşturuyoruz.

activity_main.xml
<script src="https://gist.github.com/alikaraca/765bc4a50e9ce57278902c352d59a3f3.js"></script>

MainActivity.java
<script src="https://gist.github.com/alikaraca/84c7b78fb79af008c0a78700003d3a36.js"></script>

## RadioButton ve RadioGroup Örneği

Bu örneğimizde de edittextimize işlem yapacağımız iki sayı giriyoruz ve radiobutondan işlemimizi seçiyoruz.RadioGroup kullanarak radiobutonlardan bir tane seçmemizi sağlıyoruz.

activity_main.xml

<script src="https://gist.github.com/alikaraca/88e83d7240db6a2dbfb68c7cd9f09635.js"></script>

MainActivity.java

<script src="https://gist.github.com/alikaraca/9f60cfcc2cf518e66a6af675aaaf3926.js"></script>

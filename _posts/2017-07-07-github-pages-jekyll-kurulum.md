---
layout: post
title: "Github Pages ve Jekyll Kurulumu"
date: 2017-07-07
excerpt: "Github Pages ve Jekyll"
tags: [github pages, jekyll, blog]
comments: true
---
## **Github Pages Nedir?**

Github, kullanıcılarına Github Depoları(Repositories) üzerinden yönetilebilen hosting sağlamaktadır.En önemlisi de bunu ücretsiz sağlamaktadır.Eğer kendi blog sitenizi kurmak istiyorsanız ve hosting için para vermek istemiyorsanız github pages'i kullanabilirsiniz.

## **Github Pages Kurulumu**

Github pages kurulumu için ilk olarak repository oluşturun ve **_kullanıcıisminiz.github.io_** olarak ayarlayın.

<figure>
   <a href="/assets/img/github pages.png">
   <img src="/assets/img/github pages.png"></a>
</figure>
 
Daha sonra deneme yapmak için index.html dosyasını ekleyelim ve içini aşağıdaki şekilde dolduralım.
<figure>
    <a href="/assets/img/index.png"><img                                           
    src="/assets/img/index.png"></a>
</figure>
Buradan sonra da aşağıdan commit new file butonuna tıklayarak dosyamızı oluşturmuş olduk.
Şimdi de tarayıcınızın url bölümüne **_kullanıcıisminiz.github.io_** yazarak sitenizi test edebilirsiniz.
<figure>
   <a href="/assets/img/dsadadasdas.png"><img
   src="/assets/img/dsadadasdas.png"></a>
</figure>
Gördüğünüz gibi sitemiz aktif hale gelmiştir.Şimdi de jekyll kurulumunu geçelim.

## **Jekyll Nedir?**

<figcaption><a href="https://jekyllrb.com/">Jekyll</a> ruby ile yazılmış basit ve güçlü bir altyapıya sahip olan statik bir site

oluşturucudur.Markdown formatında yazdığımız sayfayı statik HTML sayfasına dönüştürür.Jekyll Github Pages tarafından desteklenen bir
mekanizmadır.

<h2>Jekyll Kurulumu</h2>

Jekyll Ruby ile yazılmış olduğu için ilk olarak Ruby kurulmalıdır.Aşağıda işletim sistemlerine göre kurulumu anlatacağım.

<h3>Windows İçin</h3>

Eğer Windows kullanıyorsanız aşağıdaki linkten Ruby'i kurmalısınız.
Ruby link: https://rubyinstaller.org/downloads/
Jekyll'ın düzgün bir şekilde çalışabilmesi için yukarıdaki linkten Development Kit'i indirmelisiniz.
Development Kit'i indirip çalıştırdıktan sonra dosyaları bir yere çıkartmanızı isteyecektir.
Benim önerim C:\\DevKit buraya kurmanızdır.Bunun sebebi ise Komut İstemi(Namıdeğer cmd) de çalışırken zorlanmamamız.
Dosyalarımızı çıkardıktan sonra cmd yi açalım ve aşağıdakini yazalım.

**_cd C:\\DevKit_**

Bu dizine girdikten sonra;

**_ruby dk.rb init_**

komutunu yazalım.Daha sonra aşağıdaki komutu yazalım;

**_ruby dk.rb install_**

komutunu yazdıktan sonra Ruby'nin kurulumu tamamlandı.Kurulumunun başarılı olup olmadığını anlamak için cmd yi açarak aşağıdaki komutları yazalım.

**_ruby -v_**

**_gem -v_**

Versiyon numaraları çıkarsa kurulum başarılıdır.

---
layout: post
title: "Github Pages ve Jekyll Kurulumu"
date: 2017-07-07
excerpt: "Github Pages ve Jekyll"
tags: [github pages, jekyll, github pages ve jekyll kurulumu]
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
## Tema Kullanımı
Tema yapmak için uğraşmak istemeyip hazır tema kullanmak isterseniz.
<figcaption>
<a href="http://jekyllthemes.org/">Hazır temalar</a> linkine tıklayınız.
</figcaption>
<h2>Jekyll Nedir?</h2>

<figcaption>
   <a href="https://jekyllrb.com/" title="Jekyll">Jekyll</a> ruby ile yazılmış basit ve güçlü bir altyapıya sahip olan statik bir site oluşturucudur.Markdown formatında yazdığımız sayfayı statik HTML sayfasına dönüştürür.Jekyll Github Pages tarafından desteklenen bir mekanizmadır.
</figcaption>

<h2>Jekyll Kurulumu</h2>

Jekyll Ruby ile yazılmış olduğu için ilk olarak Ruby kurulmalıdır.Aşağıda işletim sistemlerine göre kurulumu anlatacağım.

<h3>Windows İçin</h3>
<section>
<p>
   Eğer Windows kullanıyorsanız aşağıdaki linkten Ruby'i kurmalısınız.<br>
   Ruby link: <a href="https://rubyinstaller.org/downloads">Ruby</a><br>
   Jekyll'ın düzgün bir şekilde çalışabilmesi için yukarıdaki linkten Development Kit'i indirmelisiniz.<br>
   Development Kit'i indirip çalıştırdıktan sonra dosyaları bir yere çıkartmanızı isteyecektir.<br>
   Benim önerim C:\\DevKit buraya kurmanızdır.Bunun sebebi ise Komut İstemi(Namıdeğer cmd) de çalışırken zorlanmamamız.<br>
   Dosyalarımızı çıkardıktan sonra cmd yi açalım ve aşağıdakini yazalım.<br>

{% highlight html %}
cd C:\\DevKit
{% endhighlight %}
Bu dizine girdikten sonra;<br>
{% highlight html %}
ruby dk.rb init
{% endhighlight %}

komutunu yazalım.Daha sonra aşağıdaki komutu yazalım;<br>
{% highlight html %}
ruby dk.rb install
{% endhighlight %}
komutunu yazdıktan sonra Ruby'nin kurulumu tamamlandı.Kurulumun başarılı olup olmadığını anlamak için cmd yi açarak aşağıdaki komutları yazalım.<br>


{% highlight html %}
ruby -v
gem -v
{% endhighlight %}

Versiyon numaraları çıkarsa kurulum başarılıdır.<br>
Ruby ve RubyGem kurulumu tamamlandıktan sonra şimdi sıra Jekyll kurulumuna geldi.Jekyll kurulumunu yapmak için cmd yi açarak aşağıdaki komutu yazmamız gerekli;
{% highlight html %}
gem install jekyll
{% endhighlight %}
Ve Jekyll kurulumunu tamamladık.

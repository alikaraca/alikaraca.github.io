---
layout: post
title: "Android Lokal Veritabanı Olarak SQLite"
date: 2017-07-14
excerpt: "Android SQLite"
tags: [SQLite,veritabanı,android]
comments: true
---
Android ile ilgili merak edilen konulardan birisi de veritabanı kullanımıdır.Günümüzde popüler olan veritabanları Microsoft SQL Server, MySQL, Oracle vb. dir.
Ancak Android'den bunlara doğal yöntemler ile erişmek mümkün değildir, çünkü gerekli kütüphaneler bulunmamaktadır.Bu veritabanları büyüklükleri sebebiyle
Android cihazına kurulamazlar.Bu veritabanlarına ancak bir web servis aracılığıyla erişilebilir.

Android'te lokal veritabanı olarak sadece SQLite isimli dosya tipi veritabanı yönetim sistemi kullanılabilir.SQLite açık kaynak kodlu bu sebeple
birçok platformda kullanılabilir.SQLite ilişkisel ve işlemsel güçlü bir veritabanıdır.Android'in rehber, ajanda gibi kendi uygulamalarında da bu veritabanı
kullanılır.

## SQLite

SQLite, diğer sunucu tipi veritabanları ile karşılaştırıldığında basit kalmaktadır.Bu veritabanının;

*View ve trigger desteği vardır.

*Şu anda stored procedure desteği yoktur.

*Geçici tablolar oluşturulabilir.

*Desteklenen türler(Integer, null, blob, text ve real) olup dinamik tür belirlemeyi destekler.

*Diğer veritabanlarına göre desteklediği veri türü sınırlıdır.(Boolean, Datetime, Money, XML gibi türleri desteklemez.)

## SQLite İçin Kullanılan Sınıflar

SQLite veritabanı yönetim sisteminin Android'te kullanılan belli bazı sınıfları mevcuttur.

1)SQLiteOpenHelper:Veritabanı erişimi için yazılacak olan sınıf için taban sınıf olarak kullanılır.Soyut bir sınıftır.Tabloların yaratılması ya da
şematik değişiklikler bu sınıflar ile gerçekleştirilir.

2)SQLiteDatabase:CRUD(Create Read Update Delete) işlemlerini barındıran sınıftır.

3)ContentValues:Parametre değerlerinin oluşturulması amacıyla kullanılır.

4)Cursor:Veritabanından elde edilen kayıtların üzerinde çalışmaya yarayan bir interface'dir.Cursor interface'ini implemente eden SQLiteCursor
gibi sınıflar mevcuttur.ç

5)SimpleCursorAdapter:Cursor nesnesini kullanıcı arayüzünde ListView,GridView gibi kontrollere bağlarken bu sınıf kullanılır.

## Veritabanının Oluşturulması

Veritabanı oluşturmak için iki yöntem bulunmaktadır.Bunlardan birincisi kod yoluyla çalışma zamanında oluşturmak.İkincisi ise 3.parti bir araç
kullanılarak oluşturulan veritabanının projede kullanılmasıdır.Ben ise şimdi ilk yöntem ile yaptığım bir programı anlatacağım.
Bu programda 2 edittext bulunmakta bunlara girdiğimiz iki değer ekle butonu kullanılarak veritabanına eklenmekte.Sil butonu ile edittextlere silmek 
istediğimiz değerleri giriyoruz ve girdiğimiz değeri veritabanından silmekte.Listele butonu ile de veritabanında bulunan değerleri listeliyoruz.

activity_main.xml
<script src="https://gist.github.com/alikaraca/3792636b36f96ba74ffb5498e073699d.js"></script>

MainActivity.java
<script src="https://gist.github.com/alikaraca/43b12a9001754b31cf95b3ec3ec304e8.js"></script>

Veritabanı.java
<script src="https://gist.github.com/alikaraca/71830c4b4e95a6f9e2b5981d80dfe184.js"></script>



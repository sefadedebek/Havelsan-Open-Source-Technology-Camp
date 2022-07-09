# 1. isim adlı bir değişlene bir isim tanımlanarak bunun ekrana yazdırılması

input1;

```
ubuntut@ub20:~$ echo $PATH
```


output1;

```
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```


input2;

```
ubuntut@ub20:~$ isim="Havelsan Açık Kaynak Teknoloji Kampından Sefa Dedebek"
ubuntut@ub20:~$ echo $isim
```


output2;

```
Havelsan Açık Kaynak Teknoloji Kampından Sefa Dedebek
```


# 2. isim ve soyisim değişkenleri tanımlanarak bunlara birer değeri verilmeli, bunların birleştirilmiş halleri bir kisi değişkenine eşitlenmeli ve kişi değişkeni ekrana yazdırılmalı.
 
 
input1;

```
ubuntut@ub20:~$ echo $PATH
```


output1;

```
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```


input2;

```
ubuntut@ub20:~$ isim="sefa"
ubuntut@ub20:~$ soyisim="dedebek"
ubuntut@ub20:~$ kisi=$isim+$soyisim
ubuntut@ub20:~$ echo $kisi
```


output2;

```
sefa+dedebek
```
 
 

# 3. /home/ dizininde iken /etc/systemd/system dizinine tek komut ile gidilmeli.



```
ubuntut@ub20:/home$  cd /etc/systemd/system
ubuntut@ub20:/etc/systemd/system$
```

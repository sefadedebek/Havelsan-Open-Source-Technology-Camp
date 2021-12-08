# 1. bash ve sh kabuklarının çevre değişkenlerini kıyaslama



## 1.1. Bir uçbirim açın ve mevcut kabuğu ekrana yazdırın




mevcut çekirdek sürümü

input;

```
ubuntut@ub20:~$ cat /proc/version
```


output;

```
Linux version 5.4.0-91-generic (buildd@lcy01-amd64-017) (gcc version 9.3.0 (Ubuntu 9.3.0-17ubuntu1~20.04)) #102-Ubuntu SMP Fri Nov 5 16:31:28 UTC 2021
```




yüklü gelen kabuklar


input;

```
cat /etc/shells 

```



output;


```
/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/bin/dash
/usr/bin/dash
/usr/bin/tmux
/usr/bin/screen
```


## 1.2. bash kabuğuna geçerek çevre değişkenlerini ekrana yazdırın


input;

```
ubuntut@ub20:~$ chsh
Changing the login shell for ubuntut
Enter the new value, or press ENTER for the default
        Login Shell [/bin/bash]: /bin/bash

ubuntut@ub20:~$ printenv
```



output;

```
SHELL=/bin/bash
PWD=/home/ubuntut
LOGNAME=ubuntut
XDG_SESSION_TYPE=tty
MOTD_SHOWN=pam
HOME=/home/ubuntut
LANG=en_US.UTF-8
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=30;41:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.dz=01;31:*.gz=01;31:*.lrz=01;31:*.lz=01;31:*.lzo=01;31:*.xz=01;31:*.zst=01;31:*.tzst=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.alz=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.cab=01;31:*.wim=01;31:*.swm=01;31:*.dwm=01;31:*.esd=01;31:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:
SSH_CONNECTION=192.168.43.174 6152 192.168.43.10 22
LESSCLOSE=/usr/bin/lesspipe %s %s
XDG_SESSION_CLASS=user
TERM=xterm-256color
LESSOPEN=| /usr/bin/lesspipe %s
USER=ubuntut
SHLVL=1
XDG_SESSION_ID=11
XDG_RUNTIME_DIR=/run/user/1000
SSH_CLIENT=192.168.43.174 6152 22
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
SSH_TTY=/dev/pts/0
_=/usr/bin/printenv
```


## 1.3.sh kabuğuna geçerek çevre değişkenlerini ekrana yazdırın


input;

```
ubuntut@ub20:~$ chsh
Changing the login shell for ubuntut
Enter the new value, or press ENTER for the default
        Login Shell [/bin/bash]: /bin/sh

ubuntut@ub20:~$ printenv
```


output;

USER=ubuntut
SSH_CLIENT=192.168.43.174 14281 22
XDG_SESSION_TYPE=tty
HOME=/home/ubuntut
MOTD_SHOWN=pam
SSH_TTY=/dev/pts/0
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
LOGNAME=ubuntut
XDG_SESSION_CLASS=user
TERM=xterm-256color
XDG_SESSION_ID=5
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
XDG_RUNTIME_DIR=/run/user/1000
LANG=en_US.UTF-8
SHELL=/bin/sh
PWD=/home/ubuntut
SSH_CONNECTION=192.168.43.174 14281 192.168.43.10 22
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop





# 2. Python kabuğu üzerinde basit fonksiyon geliştirme



## 2.1. Uçbirim üzerinde python kabuğu açılmalı, python kabuğu üzerinde fibo (fibınacci dizisi için) kütüphanesini içeri aktararak, dizinin ilk 10 sayısını döndüren bir fonksiyon yazın.


"fibo.py" isimli Python dosyası açana kadar olan işlemler;
input;

```
ubuntut@ub20:~$ python3 -V
Python 3.8.10
ubuntut@ub20:~$ sudo apt install -y python3-venv
ubuntut@ub20:~$ mkdir environments
ubuntut@ub20:~$ cd environments
ubuntut@ub20:~/environments$ cd environments
-bash: cd: environments: No such file or directory
ubuntut@ub20:~/environments$ python3 -m venv my_env

ubuntut@ub20:~/environments$
ubuntut@ub20:~/environments$ python3 -m venv my_env
ubuntut@ub20:~/environments$ ls my_env
bin  include  lib  lib64  pyvenv.cfg  share
ubuntut@ub20:~/environments$ source my_env/bin/activate
(my_env) ubuntut@ub20:~/environments$
(my_env) ubuntut@ub20:~/environments$ nano fibo.py

```


Python Kodu;

```
# Python program to display the Fibonacci sequence

def recur_fibo(n):
   if n <= 1:
       return n
   else:
       return(recur_fibo(n-1) + recur_fibo(n-2))

nterms = 10

# check if the number of terms is valid
if nterms <= 0:
   print("Plese enter a positive integer")
else:
   print("Fibonacci sequence:")
   for i in range(nterms):
       print(recur_fibo(i))
```

Python Kodunu Derleme ve Koşturma;

```
(my_env) ubuntut@ub20:~/environments$ python fibo.py
```

output;

```
Fibonacci sequence:
0
1
1
2
3
5
8
13
21
34
```



# 3. Kullanıcı bazlı değil, sistem genelinde kalıcı bir çevre değişkeni tanımlanmak istense, hangi sistem dosyası kullanılabilir.

Kullanıcı bazlı değil, sistem genelinde kalıcı bir çevre değişkeni tanımlanmak istense, /etc/environment dosyası kullanılabilir . 
Alternatif bir yol ise, /etc/profile.d dizininde bir dosya oluşturmaktır .


# 4. Kullanıcı ana dizininde bulunan dosyalardan hangisi Bash geçmişini depolamak için kullanılır?


bash_history
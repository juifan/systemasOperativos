# Comandos Bash
#

### date -u +"%Y-%m-%d" 
Muestra año a cuatro digitos mes y dia
~~~
2019-05-03
~~~

### which $PROGRAMA 
muestra la ruta absoluta del programa  
~~~
cristian@Cristian-pc:~$ which firefox
/usr/bin/firefox
~~~
### ps 
Muestra los procesos activos en ese momento en esa sesion
~~~
cristian@Cristian-pc:~$ ps
  PID TTY          TIME CMD
 3135 pts/0    00:00:00 bash
 3298 pts/0    00:00:00 ps

~~~
### history 
muestra el historial de la temrinal
~~~
cristian@Cristian-pc:~$ history
    1  help
    2  ls
    3  cd Music
    4  ls
    5  cd..
    6  cd
    7  cd..
    8  cat Music
    9  clear
   10  bash
   ....
~~~
### less  
puede navegar en el texto que recibe como parametro
~~~
cristian@Cristian-pc:~/Desktop$ less prueba
Comandos bash
~
~
(END)
~~~
### who  
Muestra el usuario activo
~~~
cristian@Cristian-pc:~/Desktop$ who
cristian tty7   2019-05-03 08:43 (:0)
~~~
### uptime  
muestra el tiempo que lleva encendido el equipo
~~~
cristian@Cristian-pc:~/Desktop$ uptime
 10:43:51 up  2:03,  1 user,  load average: 0.99, 1.04, 1.28
~~~
### telnet $IP $PORT
sirve para emular una terminal remota donde recibe una ip y el puerto como parametros
~~~
cristian@Cristian-pc:~/Desktop$ telnet 125.64.124.77
~~~

### sudo $COMANDO
permite al usuario de un sistema acceder a los privilegios de seguridad de otro usuario.
~~~
su -c "apt install nmap
~~~
### nmap -Pn $IP
Muestra informacion de la ip ingresada
~~~
cristian@Cristian-pc:~/Desktop$ nmap -Pn 127.0.0.1
Starting Nmap 7.40 ( https://nmap.org ) at 2019-05-03 11:20 CDT
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00046s latency).
Not shown: 999 closed ports
PORT    STATE SERVICE
631/tcp open  ipp

Nmap done: 1 IP address (1 host up) scanned in 0.19 seconds

~~~
### traceroute $IP
Se usa para determinar la ruta que toma un paquete de protocolo de Internet (IP) para alcanzar su destino.
~~~
cristian@Cristian-pc:~/Desktop$ traceroute 127.0.0.1
traceroute to 127.0.0.1 (127.0.0.1), 30 hops max, 60 byte packets
 1  localhost (127.0.0.1)  0.091 ms  0.056 ms  0.049 ms
~~~
### bc
Realiza operaciones matematicas
~~~
cristian@Cristian-pc:~/Desktop$ bc
bc 1.06.95
Copyright 1991-1994, 1997, 1998, 2000, 2004, 2006 Free Software Foundation, Inc.
This is free software with ABSOLUTELY NO WARRANTY.
For details type `warranty'. 
5+6
11
~~~
### ping $IP
Permite comprobar de una manera sencilla si tu equipo está conectado a Internet
~~~
cristian@Cristian-pc:~/Desktop$ ping 127.0.0.1
PING 127.0.0.1 (127.0.0.1) 56(84) bytes of data.
64 bytes from 127.0.0.1: icmp_seq=1 ttl=64 time=0.087 ms
64 bytes from 127.0.0.1: icmp_seq=2 ttl=64 time=0.150 ms
64 bytes from 127.0.0.1: icmp_seq=3 ttl=64 time=0.146 ms
64 bytes from 127.0.0.1: icmp_seq=4 ttl=64 time=0.151 ms
64 bytes from 127.0.0.1: icmp_seq=5 ttl=64 time=0.057 ms
~~~
### uso del simbolo pipe " | "
Consiste en una cadena de procesos conectados de forma tal que la salida de cada elemento de la cadena es la entrada del próximo.
~~~
cristian@Cristian-pc:~$ ls -a | more
.
..
.bash_history
.bash_logout
.bashrc
.cache
.cinnamon
.config
Desktop

~~~
### redirección de salida inversa " < "
Redirecciona un salida a un comando 
~~~
cristian@Cristian-pc:~/Desktop$ wc -l  < prueba
75
~~~
### top
Produce una lista ordenada de procesos en ejecución seleccionados por criterios especificados por el usuario y los actualiza periódicamente.
~~~
cristian@Cristian-pc:~/Desktop$ top

top - 11:46:55 up  3:06,  1 user,  load average: 1.15, 1.31, 1.28
Tasks: 153 total,   1 running, 152 sleeping,   0 stopped,   0 zombie
%Cpu(s):  8.3 us,  5.0 sy,  0.0 ni, 83.0 id,  3.7 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :  3930952 total,  1347400 free,  1431784 used,  1151768 buff/cache
KiB Swap:  4073468 total,  4073468 free,        0 used.  2114480 avail Mem 

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND     
 1355 cristian  20   0 1848416 232696  50228 S   8.3  5.9  14:24.80 cinnamon    
  672 root      20   0  379716  71180  40428 S   7.6  1.8   8:23.95 Xorg        
 1586 cristian  20   0 2772412 448892 141780 S   7.0 11.4  35:19.88 firefox-esr 
 3866 cristian  20   0  629684  35204  27328 S   4.0  0.9   0:03.95 gnome-term+ 
 1250 cristian   9 -11 1952640  19832  16744 S   3.3  0.5   5:42.63 pulseaudio  
 1706 cristian  20   0 1961516 239664 126588 S   0.7  6.1   9:07.95 Web Content 
 1750 cristian  20   0 2276924 357276 118708 S   0.7  9.1  34:17.70 Web Content 
 4049 cristian  20   0   44904   3712   3124 R   0.7  0.1   0:01.41 top 
~~~
### sleep $Ns #donde N es un numero
Se utiliza para temporizar un intervalo de tiempo determinado. La unidad de tiempo por defecto es el segundo.
~~~
cristian@Cristian-pc:~/Desktop$ sleep 5
~~~




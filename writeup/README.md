<h3>In this challenge you are given a simple binary</h3>
<h3> Runing the binary..it is asking for pasword</h3>

```./0x41haz.0x41haz 
=======================
Hey , Can You Crackme ?
=======================
It's jus a simple binary 

Tell Me the Password :
1111
Is it correct , I don't think so.
```

<h3>Lets run the file command</h3>

```file 0x41haz.0x41haz 
0x41haz.0x41haz: ELF 64-bit MSB *unknown arch 0x3e00* (SYSV)
```
<h3>its an anti reversing technique you have to bypass it .hmm.. how can we do that ??? for that, you need to patch the sixth byte(0x02) to 0x01 as given
  below</h3>
 <img align="centre" alt="IMG" src="https://github.com/0x41haz/challenges/blob/main/writeup/2021-12-24_15-05.png?raw=true" width="500" height="70" />

<h3>Now look</h3>

```file 0x41haz.0x41haz 
0x41haz.0x41haz: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=6c9f2e85b64d4f12b91136ffb8e4c038f1dc6dcd, for GNU/Linux 3.2.0, stripped
```
<h3>It is an stripped binary .lets open with radare2. looking at the main function as [pdf @main]</h3>
 <img align="centre" alt="IMG" src="https://github.com/0x41haz/challenges/blob/main/writeup/main-fun.png?raw=true" width="1500" height="900" />

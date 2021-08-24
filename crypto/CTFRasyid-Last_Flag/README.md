![Soal](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Last_Flag/soal.png?raw=true)

Dibersi sebuah teks yang sudah dienkripsi :
```
HEFX{q4dt_im4113yg3?}
```

Setelah mencoba beberapa algoritma cipher, diketahui bahwa teks tersebut dienskripsi menggunakan Viginere Cipher. 

Kemudian saya membruteforce key nya menggunakan teknik known-plaintext word dengan tool di web [https://www.dcode.fr/vigenere-cipher](https://www.dcode.fr/vigenere-cipher). 

![Solver](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Last_Flag/solver.png?raw=true)



Setelah dijalankan, diketahui bahwa flag tersebut menggunakan key 'flag' untuk Viginere Cipher nya

![Output](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Last_Flag/output.png?raw=true)


> FLAG : CTFR{l4st_ch4113ng3?}


### CTF Rasyid - Dasar64

![Soal](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Dasar64/soal.png?raw=true)

Diberikan teks : 
```
Q1RGUntzMW1wbDNfYjRzM182NH0=
```

Berdasarkan nama soalnya, 'Dasar64' atau dalam bahasa inggris 'Base64' berarti teks ini merupakan hasil encoding dari base64 encoder. 

Oleh karena itu, saya mendecode tekst tersebut menggunakan perintah pada linux : 
```
echo 'Q1RGUntzMW1wbDNfYjRzM182NH0=' | base64 -d
```

Setelah menjalankan perintah tersebut, maka flagnya akan muncul. 
![Soal](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Dasar64/solver.png?raw=true)

> Flag : CTFR{s1mpl3_b4s3_64}
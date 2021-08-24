![Soal](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Second_Flag/soal.png?raw=true)

Dibersi sebuah teks yang sudah dienkripsi :
```
TKWI{j3t0eu_wc4x_n4j_t1gy3i_k3ok}
```

Setelah dianalisis, diketahui bahwa teks tersebut dienskripsi menggunakan CAESAR Cipher. 

Kemudian saya membuat script dari python yang membruteforce nilai dari _shift_ nya. 

```python
key = 'abcdefghijklmnopqrstuvwxyz'
KEY = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'

def encrypt(n, plaintext):
	for l in plaintext:
		try:
			if l.isupper():
				index = KEY.index(l)
				i = (index +n) % 26
				result += KEY[i]
			else:
				index = key.index(l)
				i = (index +n) % 26
				result += key[i]
		except ValueError:
			result+=l
	return result


def decrypt(n, chipertext):
	result = ''

	for l in chipertext:
		try:
			if l.isupper():
				index = KEY.index(l)
				i = (index -n) %26
				result += KEY[i]
			else:
				index = key.index(l)
				i = (index-n)%26
				result +=key[i]
		except ValueError:
			result += l 

	return result

chipertext = 'TKWI{j3t0eu_wc4x_n4j_t1gy3i_k3ok}'

for n in range(0,27):
	dec = decrypt(n ,chipertext)
	print("{} : {}".format(n,dec)) 
```

Setelah dijalankan, diketahui bahwa flag tersebut menggunakan alphabet shift 17 untuk Caesar Cipher nya
![Output](https://github.com/robisetiapermadi/my-ctf-writeups/blob/master/crypto/CTFRasyid-Second_Flag/output.png?raw=true)

> FLAG : CTFR{s3c0nd_fl4g_w4s_c1ph3r_t3xt}


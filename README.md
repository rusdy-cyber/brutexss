# BruteXSS

BruteXSS - Cross-Site Scripting BruteForcer

Author: [Shawar Khan, rusdi]

**The BruteXSS project is sponsored and supported by [Netsparker Web Application Security Scanner](https://www.netsparker.com/?utm_source=github.com&utm_medium=referral&utm_content=brand+name&utm_campaign=generic+advert)**

Disclaimer: Saya tidak bertanggung jawab atas segala kerusakan yang terjadi menggunakan alat ini. Alat ini hanya boleh digunakan untuk tujuan pendidikan dan untuk pengujian penetrasi.


### Compatibility: 
* Windows , Linux or any device running python 2.7

### Requirements: 

* Python 2.7

* Wordlist included(wordlist.txt)

* Modules required: Colorama, Mechanize


### Modules Required:

* Colorama:  https://pypi.python.org/pypi/colorama/

* Mechanize: https://pypi.python.org/pypi/mechanize/


### Description:
**BruteXSS** adalah Brutforcer Skrip Lintas Situs yang sangat kuat dan cepat yang digunakan untuk memaksa parameter. BruteXSS menyuntikkan beberapa payload yang dimuat dari daftar kata tertentu dan mengaktifkannya pada parameter yang ditentukan dan memindai apakah ada parameter yang rentan terhadap kerentanan XSS. BruteXSS sangat akurat dalam melakukan tugasnya dan tidak ada kemungkinan kesalahan positif karena pemindaiannya sangat kuat. BruteXSS mendukung permintaan POST dan GET yang membuatnya kompatibel dengan aplikasi web modern.

### Features:

* XSS Bruteforcing

* XSS Scanning

* Supports GET/POST requests

* Custom wordlist can be included

* User-friendly UI

### Usage(GET Method):

```
COMMAND:  python brutexss.py
METHOD:   g
URL:      http://www.site.com/?parameter=value
WORDLIST: wordlist.txt
```

### Usage(POST method):

```
COMMAND:   python brutexss.py
METHOD:    p
URL:       http://www.site.com/file.php
POST DATA: parameter=value&parameter1=value1
WORDLIST:  wordlist.txt
```

### Output:

```
  ____             _        __  ______ ____  
 | __ ) _ __ _   _| |_ ___  \ \/ / ___/ ___| 
 |  _ \| '__| | | | __/ _ \  \  /\___ \___ \ 
 | |_) | |  | |_| | ||  __/  /  \ ___) |__) |
 |____/|_|   \__,_|\__\___| /_/\_\____/____/ 
                                            
 BruteXSS - Cross-Site Scripting BruteForcer
 
 Author: Shawar Khan - https://shawarkhan.com                      


Select method: [G]ET or [P]OST (G/P): p
[?] Enter URL:
[?] > http://site.com/file.php
[+] Checking if site.com is available...
[+] site.com is available! Good!
[?] Enter post data: > parameter=value&parameter1=value1
[?] Enter location of Wordlist (Press Enter to use default wordlist.txt)
[?] > wordlist.txt
[+] Using Default wordlist...
[+] Loading Payloads from specified wordlist...
[+] 25 Payloads loaded...
[+] Injecting Payloads...

[+] Testing 'parameter' parameter...
[+] 2 / 25 payloads injected...
[!] XSS Vulnerability Found! 
[!] Parameter:	parameter
[!] Payload:	"><script>prompt(1)</script>

[+] Testing 'parameter1' parameter...
[+] 25 / 25 payloads injected...
[+] 'parameter1' parameter not vulnerable.
[+] 1 Parameter is vulnerable to XSS.
+----+--------------+----------------+
| Id | Parameters   |     Status     |
+----+--------------+----------------+
| 0  |  parameter   |  Vulnerable    |
+----+--------------+----------------+
| 1  |   parameter1 | Not Vulnerable |
+----+--------------+----------------+

```

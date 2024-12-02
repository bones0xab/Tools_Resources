# Gobuster
gobuster dir -u http://10.10.10.10 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 50 -x.php

-x : specific file extension
-k : disable check certificate error
--exclude-length: exclude specific length not to display
-o: for output
-f: add / at the end of the file
-n: not to print specific status code
-w: wordlist
-t for thread

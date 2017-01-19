# WeevBot
Browser Based DNS Exfiltration

Disclaimer: This project is a proof of concept. We don't condone doing
illegal activities with this code. Only use this example against targets
that you own/control and have permission to target. Also, this code comes
without any warranty, it might kills kittens so just don't.

The talk that explains these files is here:
https://www.youtube.com/secdsm

Files:
client_example.html - Code to run in the unsuspecting user's browser to extract text from baconipsum.com
and exfiltrate the contexts to exfil.example.com

example_zone.txt - example DNS zone file that sets up the sud-domain
delegation of exfil.example.com.

simpledns.py - example DNS server in python. Copied from https://gist.github.com/pklaus/b5a7876d4d2cf7271873

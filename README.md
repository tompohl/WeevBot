# WeevBot
Browser Based DNS Exfiltration

Disclaimer: This project is a proof of concept. We don't condone doing
illegal activities with this code. Only use this example against targets
that you own/control and have permission to target. Also, this code comes
without any warranty, it might kill kittens so just don't.

The talk that explains these files is here:
https://www.youtube.com/secdsm

Files:
client_example.html - Code to run in the unsuspecting user's browser to extract text from baconipsum.com
and exfiltrate the contexts to exfil.example.com

example_zone.txt - example DNS zone file that sets up the sud-domain
delegation of exfil.example.com.

simpledns.py - example DNS server in python. Copied from https://gist.github.com/pklaus/b5a7876d4d2cf7271873

get_ids - show ids collected from unsuspecting users

get_id <id_num> - show data collected

To run the server:
python34 simpledns.py --port 53 --tcp --udp >> output.log

Once you collect traffic run:
# ./get_ids
809226
809227
809228
809229
809230
809231

# ./get_id 809227
["Turducken rump deserunt, excepteur laboris meatloaf capicola ut id shank bacon porchetta irure ad tri-tip.  Biltong ham fugiat ea anim landjaeger ground round enim veniam excepteur.  In quis cupim in chicken deserunt incididunt ground round t-bone ex.  Chuck andouille porchetta proident.  Tongue jowl esse, veniam pig burgdoggen in bacon biltong jerky chuck.  Ut eu picanha shoulder sunt cupidatat.  Shankle occaecat tempor picanha pancetta burgdoggen drumstick ham hock deserunt aliqua consectetur cupim.","Ullamco aute pig fatback kielbasa.  Sed ex filet mignon salami velit.  Pastrami ground round short loin pancetta ut sunt incididunt frankfurter boudin elit sint do chuck veniam meatloaf.  Dolor pork loin in, velit biltong cow ut dolore.  Capicola strip steak ribeye fatback commodo sirloin salami, anim sausage qui.  Jerky flank leberkas filet mignon hamburger.","Porchetta enim dolore, ut pariatur ribeye sunt.  Non cupim irure meatball labore ut.  Id chuck prosciutto elit.  Ad sausage frankfurter proident.  Pastrami chicken salami, picanha eu pork officia ball tip aliqua.  Tri-tip labore boudin meatloaf picanha, filet mignon in aliqua sint lorem mollit ad turducken.  Hamburger ipsum kielbasa ribeye ad labore, eu flank swine porchetta.","Ut landjaeger porchetta spare ribs mollit qui beef.  Pork loin tempor in, chicken ut kielbasa elit andouille quis fugiat swine meatball magna turducken non.  In laboris mollit aliqua prosciutto picanha elit capicola.  Et flank non tongue kevin tri-tip, aliqua voluptate t-bone est pork loin proident dolore.","Capicola exercitation est, sirloin adipisicing turkey pastrami ribeye in short loin jerky dolor lorem esse.  Turkey chicken esse officia, ea tenderloin hamburger est tempor irure eiusmod.  Dolore elit id, esse ullamco bacon ground round anim incididunt.  Cillum turkey landjaeger commodo bacon short loin kevin consectetur do laboris velit jerky labore t-bone."]


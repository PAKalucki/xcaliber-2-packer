Zadanie
=======

Za pomocą Hashicorp Packer oraz basha i/lub dodatkowego narzędzia ansible, salt ( ale sam bash jest
też OK ) stwórz/zbuduj obraz virtualbox – z linuxem (Centos 7).
Obraz ten powinien posiadać
- zainstalowany nginx
- nginx skonfigurowany dla obsługi 2 vhostów których nazwy będą podawane przy budowaniu
np. 'example.com' i 'sth.pl'
- access logi każdego z vhostów mają być zapisywane do pliku /var/log/nazwa_domeny_access.log

About
=====

versions:  
VirtualBox Version 5.2.34_Ubuntu  
Ansible 2.9.6  
Packer 1.5.5  
  
packer build -var 'vhosts="example.com sth.pl"' template.json  
vhosts odzielone spacjami  

Tbh nie jestem w stanie wyjasnic czemu podczas budowania packerem nginx instaluje sie uszkodzony niezaleznie od tego jak to robie, pod odpaleniu virtualki i yum reinstall nginx wszystko dziala...
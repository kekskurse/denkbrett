1) Arch linux grundsystem installieren

* https://wiki.archlinux.de/title/Systemverschl%C3%BCsselung_mit_dm-crypt
* https://wiki.archlinux.de/title/Arch_Install_Scripts
* https://wiki.archlinux.de/title/Anleitung_f%C3%BCr_Einsteiger
* https://github.com/ejmg/an-idiots-guide-to-installing-arch-on-a-lenovo-carbon-x1-gen-6

Da ich beim einrichten von den PArtitionen erstmal versagte (boot flag war nicht zu setzten) habe ich erstmal ein ubuntu installiert um danach das arch mit syslinux zu installieren

2) netzwerk config testen

ping -c 3 google.de

2) git und ansible installieren

pacman -Suy git ansible


3) clonen des repros mit dem ansible script

git clone https://github.com/kekskurse/denkbrett.git

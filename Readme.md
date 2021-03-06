# Installation

1) Arch linux grundsystem installieren

* https://wiki.archlinux.de/title/Systemverschl%C3%BCsselung_mit_dm-crypt
* https://wiki.archlinux.de/title/Arch_Install_Scripts
* https://wiki.archlinux.de/title/Anleitung_f%C3%BCr_Einsteiger
* https://github.com/ejmg/an-idiots-guide-to-installing-arch-on-a-lenovo-carbon-x1-gen-6

Da ich beim einrichten von den PArtitionen erstmal versagte (boot flag war nicht zu setzten) habe ich erstmal ein ubuntu installiert um danach das arch mit syslinux zu installieren

2) netzwerk config testen

```
ping -c 3 google.de
```

2) git, ansible und openssh installieren

```
pacman -Suy git ansible openssh
```

2.1) install yay

```
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

2.2) Install ansible aur helper
```
git clone https://github.com/kewlfft/ansible-aur.git ~/.ansible/plugins/modules/aur
```

3) SSH-Key erzeugen und zugriff auf sich selbst geben

```
ssh-keygen
cd ~/.ssh
cat id_rsa.pub > authorized_keys
systemctl start sshd.service
```

the last line will start the ssh service until reboot the pc

3) clonen des repros mit dem ansible script

```
git clone https://github.com/kekskurse/denkbrett.git
cd denkbrett
```


4) Check if ansible work:
```
ansible -i hosts.ini all -m ping
```

6) Check the denkbrett.yml for the roles you want to use

7) Change the varieables in group:vars/pc.yml

8) Run ansible script

```
ansible-playbook -i hosts.ini denkbrett.yml
```

9) setzten eines password für den neuen nuzter
```
passwd <username>
```

10) reboot

# Update

# Roles

* common -> common stuff
* i3 -> install xorg and i3wm


# Using

* https://github.com/mnussbaum/ansible-yay

# Trabalho_SO
Buildar um kernel do linux
Itens necessários para build - Máquina virtual com sistema linux.
ISO pode ser pega aqui - https://ubuntu.com/download/desktop ou com link direto - https://ubuntu.com/download/desktop/thank-you?version=22.04&architecture=amd64

Sites utilizados:

Site para verificação de versão, documentação e afins:
https://kernel.org/

Publicação da versão 5.18.9

https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git/tree/?h=v5.18.9

Documentação sobre os requisitos minimos para build.

https://docs.kernel.org/process/changes.html

Comandos utilizados.

sudo apt-get install gcc clang make bash binutils flex bison pahole utils-linux kmod e2fsprogs jfsutils reiserfsprogs xfsprogs squashfs-tools btrfs-progs pcmciautils quota ppp nfs-common procps udev grub-install iptables openssl bc cpio

sudo apt-get install libssl-dev #libcrypto

passos para instalar o mcelog:

  git clone git://git.kernel.org/pub/scm/utils/cpu/mce/mcelog.git
  
  cd mcelog
  
  make
  
  make install
  
  
mount -t nfsd nfsd /proc/fs/nfsd # nfs-utils

Para solucionar erros encontrados:

sudo apt-get install libncurses-dev

sudo apt install qt5*

sudo apt install libelf-dev

vi .config dentro da pasta onde foi feito o git clone.

make -j$(nproc)

make modules

sudo make modules_install

sudo make install

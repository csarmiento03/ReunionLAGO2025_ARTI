En este repositorio se encuentran los archivos necesarios para el taller de ARTI.

Paquetes de perl necesarios para correr ARTI
```
yum install perl-libwww-perl  
yum install epel-release
yum install perl-JSON perl-libwww-perl perl-CPAN
yum install perl-LWP-Protocol-https openssl-devel

export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```
```
for i in DAT??????.bz2; do j=$(echo $i | sed -e 's/.bz2//'); u=$(echo $j | sed -e 's/DAT//'); bzip2 -d -k $i; echo $j | ../../../arti/analysis/lagocrkread | ../../../arti/analysis/analysis -p -v $u; rm $j; done

bzcat *sec.bz2 | ../../../arti/analysis/showers -a 10 -d 10 -c 5100. -n 1 1 -v salida_apx_foton
```
bzcat *sec.bz2 | ../../../arti/analysis/showers -a 10 -d 10 -c 5100. -n 1 1 -v salida_apx

sudo docker cp 86f868b24fda:/opt/lago-corsika-77402/run/lagoW_000300/salida_bga_300.shw.bz2 /home/christian/Documentos/Workshop_LAGO

# nota-install-ubuntu-server

<h1>Intruções e dicas de como montar os servidor</h1>
<h2>Maquina virtual em Hyper-V</h2>
<p>- Criar comutador virtual para rede externa para comunicar ips</p>
<p>- a mascara de rede estav no formto e sequancia:</p>
<p>- mascara: 192.168.1.0/24</p>
<p>- ip servidor: 192.168.1.54</p>
<p>- 192.168.1.1</p>
<p>- 8.8.8.8</p>

<h2>colocando ip fixo</h2>
<p>crie uma arquivo de interface de rede</p>
	
	sudo nano /etc/netplan/01-netcfg.yaml
</br>
<p>coloque as informações no arquivo</p>
<code>network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: no
      addresses:
        - 192.168.1.100/24
      gateway4: 192.168.1.1
      nameservers:
        addresses:
          - 8.8.8.8
          - 8.8.4.4
</code>         
</br>
<p>crie uma arquivo de interface de rede</p>
	
	sudo netplan apply
</br>
</br>
<p>Link pra acesso SSH</p>
	
	https://mobaxterm.mobatek.net/download.html
</br>

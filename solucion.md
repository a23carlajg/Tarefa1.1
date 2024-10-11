# 1.1 Instalación de zonas mestras primarias

1. Instala o servidor BIND9 no equipo darthvader. Comproba que xa funciona coma servidor DNS caché pegando no documento de entrega a saída deste comando:
#### dig @localhost www.edu.xunta.es 

![captura](imaxes/Captura)

2. Configura o servidor BIND9 para que empregue como reenviador 8.8.8.8. pegando no documento de entrega contido do ficheiro 
#### /etc/bind/named.conf.options 
![captura2.1](imaxes/Captura2.1)

e a saída deste comando: 

#### dig @localhost www.mecd.gob.es

![captura2](imaxes/Captura2) 

3. zona primaria de resolución directa "starwars.lan"
![captura3](imaxes/Captura3)

![captura4](imaxes/Captura4)

4. Instala unha zona de resolución inversa que teña que ver co enderezo do equipo darthvader, e engade rexistros PTR para os rexistros tipo A do exercicio anterior. Pega no documento de entrega o contido do arquivo de zona, e do arquivo /etc/bind/named.conf.local
![captura5](imaxes/Captura5)

![captura6](imaxes/Captura6)

5. Comproba que podes resolver os distintos rexistros de recursos. Pega no documento de entrega a saída dos comandos:

##### nslookup darthvader.starwars.lan localhost
![captura7](imaxes/Captura7)
##### nslookup skywalker.starwars.lan localhost
![captura8](imaxes/Captura8)
##### nslookup starwars.lan localhost
![captura9](imaxes/Captura9)
##### nslookup -q=mx starwars.lan localhost
![captura10](imaxes/Captura10)
##### nslookup -q=ns starwars.lan localhost
![captura11](imaxes/Captura11)
##### nslookup -q=soa starwars.lan localhost
![captura12](imaxes/Captura12)
##### nslookup -q=txt lenda.starwars.lan localhost
![captura13](imaxes/Captura13)
##### nslookup 192.168.20.11 localhost
![captura14](imaxes/Captura14)
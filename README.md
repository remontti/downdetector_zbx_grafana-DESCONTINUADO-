# Zabbix / Grafana

## Downdetector

### Requisitos

```txt
Python 3
beautifulsoup4
cloudscraper
requests
openssl 1.1.1
```

### Uso

```sh
./downdetector.py {nome site}
./downdetector.py whatsapp
```

#### Debian /Ubuntu

```sh
apt install python3-pip
pip3 install bs4
pip3 install requests
pip3 install cloudscraper
```

> Caso já tenha o pip instalado e queira instalar as dependencias rode:

```sh
pip3 install requirements.txt
```

> Copie os arquivos downdetectorDiscovery.py downdetectorlist.list downdetector.py para /usr/lib/zabbix/externalscripts, altere suas permissões para o usuários zabbix.

```sh
chown zabbix. /usr/lib/zabbix/externalscripts/downdetector*
chmod a+x /usr/lib/zabbix/externalscripts/downdetector*.py
```

## Discovery/Auto Configuração

> Edite o arquivo downdetectorlist.list e altere para 1 os sites/host que deseja monitorar.

### downdetectordiscoverylist.list

> 0 = INATIVO
>
> 1 = ATIVO

```csv
0;caixa;Caixa Econômica Federal
1;caixa;Caixa Econômica Federal
```

# supervisor-teste
Aprendendo a interagir com o programa supervisord e supervisorctl

# Comandos para instalação
python bootstrap.py -- Gera o executável do buildout

bin/buildout -- Instala os pacotes e dependências configuradas no arquivo buildout.cfg

bin/supervisord -- Inicializa o serviço supervisorctl
 
 
# Comandos úteis
tail -f var/log/supervisord.log -- Para acompanhar os logs do serviço supervisorctl
 
bin/supervisorctl status all --Lista o status dos processos do supervisor
services:flask                   RUNNING   pid 4278, uptime 0:02:39

bin/supervisorctl start all -- Inicializa os processos do supervisor

bin/supervisorctl restart all -- Reinicializa os processos do supervisor

bin/supervisorctl stop all -- Para os processos do supervisor




# supervisor-teste
Aprendendo a interagir com o programa supervisord e supervisorctl

# Comandos para instalação
python bootstrap.py -- Gera o executável do buildout

Crie o arquivo opcoes.cfg e adicione as seguintes linhas:

[buildout]

extends = buildout.cfg

[opcoes]

dir-base = # Diretório onde está o repositório

dir-python = # Diretório do executável do PYTHON

dir-web = # Localização do script que executa o serviço WEB




bin/buildout -c opcoes.cfg -- Instala os pacotes e dependências configuradas no arquivo buildout.cfg

bin/supervisord -- Inicializa o serviço supervisorctl
 
 
# Comandos úteis
tail -f var/log/supervisord.log -- Para acompanhar os logs do serviço supervisorctl
 
bin/supervisorctl status all --Lista o status dos processos do supervisor
services:flask                   RUNNING   pid 4278, uptime 0:02:39

bin/supervisorctl start all -- Inicializa os processos do supervisor

bin/supervisorctl restart all -- Reinicializa os processos do supervisor

bin/supervisorctl stop all -- Para os processos do supervisor

# Para parar o processo supervisord

ps- ewf | grep 'supervisord'  -- Este comando lista os processos que estão sendo executados relativos ao programa supervisord

kill ID_PROCESSO -- Este comando para o 'supvervisord' 


#### NodeJS

Desafio2 nodejs

Para incluir os servidors os quais irão receber a aplicação somente edite o seguinte arquivo:

    vim inventory

Para instalar o node em uma maquina nova executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t install -e "nodeins=true"

Para fazer o deploy da aplicação executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t deploy


Para fazer o Rollback da aplicação executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t rollback


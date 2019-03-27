#### NodeJS
Ansbile feito para rodar em ubuntu



#### Para incluir os servidores os quais irão receber a aplicação somente edite o seguinte arquivo:

    vim inventory

#### Para instalar o node em uma maquina nova executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t install -e "nodeins=true"

#### Para fazer o deploy da aplicação executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t deploy


#### Para fazer o Rollback da aplicação executar o comando abaixo

    sudo ansible-playbook -i inventory site.yml -t rollback

    ex. sudo ansible-playbook -i inventory site.yml  -t rollback -e "v_tag=v1.0" 
#### Para rodar os playbooks deverá existir um usuário ansible  destino.
           
          1) adduser ansible 
          2) passwd ansible
          3) vim /etc/sudoers
             ansible ALL=(ALL)  NOPASSWD: ALL
obs. para não informar a senha a todo momento, pode ser feito  trocas de  [chaves publicas!]( https://www.digitalocean.com/community/tutorials/como-configurar-chaves-ssh-no-ubuntu-18-04-pt)

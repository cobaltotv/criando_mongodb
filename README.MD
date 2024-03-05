## INSTALANDO O MONGODB PARA QUEM USA PUTTY OU A INSTANCIA DO EC2 AMAZON LINUX

#lembrando para executar todos os comandos abaixo com o super usuario

sudo su 

sudo /etc/yum.repos.d/mongodb-org-7.0.repo

## COM ELE ABERTO VAMOS INSERIR ESSE CODIGO


[mongodb-org-7.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/amazon/2023/mongodb-org/7.0/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://pgp.mongodb.com/server-7.0.asc


# FEITO ISSO VAMOS INICIAR A INSTALAÇÃO

sudo yum install -y mongodb-org

# PARA VERIFICAR O STATUS

![status](STATUS%20MONGODB.png)

sudo service mongod status

# PARA INICIAR 

sudo service mongod start


# PROXIMOS PASSOS 

cd /etc

pwd

vi mongod.conf

![all](all%20ip.png)

alterar para 0.0.0.0
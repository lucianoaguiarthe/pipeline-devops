# Container
<p align="justify">O c.</p>

## COMANDOS BÁSICOS DOCKER

<p align="justify">A c.</p>

### CRIAÇÃO DE UM CONTAINER

<p align="justify">Para criar um container execute o seguinte comando:</p> 

<p align="center"><img src="images/1.png"  width="600" height="417" align="middle"/></p>

<p align="center"><img src="images/2.png"  width="600" height="450" align="middle"/></p>

<p align="center"><img src="images/3.png"  width="800" height="372" align="middle"/></p>

<p align="center"><img src="images/4.png"  width="600" height="488" align="middle"/></p>

<p align="center"><img src="images/5.png"  width="1000" height="463" align="middle"/></p>

<p align="center"><img src="images/6.png"  width="400" height="312" align="middle"/></p>

<p align="center"><img src="images/7.png"  width="700" height="324" align="middle"/></p>

<p align="center"><img src="images/8.png"  width="1000" height="461" align="middle"/></p>

<p align="center"><img src="images/9.png"  width="1000" height="461" align="middle"/></p>

<p align="center"><img src="images/10.png"  width="1000" height="461" align="middle"/></p>



<p align="center"><img src="images/12.png"  width="1000" height="463" align="middle"/></p>

<p align="center"><img src="images/13.png"  width="1000" height="462" align="middle"/></p>

<p align="center"><img src="images/14.png"  width="1000" height="465" align="middle"/></p>

<p align="center"><img src="images/15.png"  width="1000" height="461" align="middle"/></p>

<p align="center"><img src="images/16.png"  width="850" height="522" align="middle"/></p>

<p align="center"><img src="images/17.png"  width="850" height="484" align="middle"/></p>

<p align="center"><img src="images/18.png"  width="1000" height="463" align="middle"/></p>

<p align="center"><img src="images/19.png"  width="1000" height="464" align="middle"/></p>

<p align="center"><img src="images/200.png"  width="1000" height="465" align="middle"/></p>


<p align="justify">O resulado do comando é apresentado na imagem abaixo, no qual foi realizado o download no Docker Hub da imagem do Debian e gerado um container com o nome icev</p>

<p align="center"><img src="images/admin-docker/docker-run.png"  width="700" height="109" align="middle"/></p>

<p align="justify">Explicando melhor os parâmetros do comando de criação do container:</p>

* <b>run</b> é utilizado para rodar um comando em um novo container;
* O parâmetro <b>-d</b> (deattaached) é para ser utilizado caso você não queira se conectar no container no momento de sua criação;
* O parâmetro <b>-i</b> (--interactive na sua forma estendida) é utilizado para deixar a entrada de dados ao container aberta, caso você não esteja conectado (attached) no container em questão;
* O parâmetro <b>-t</b> é utilizado para alocar um pseudo-tty para o container. Assim, podemos interagir com o interpretador de comando passando comandos para o /bin/bash, da mesma forma que usamos um terminal e uma máquina virtual ou máquina física;
* O parâmetro <b>-p</b> realiza o mapeamento das portas entre o Sistema Operacional hospedeiro e o container;
* <b>--name</b> é o nome que será atribuído ao container;
* <b>--hostname</b> é o nome de rede que será atribuído ao container.

### ACESSANDO O CONTAINER

<p align="justify">Após a instalação do container se faz necessário acessá-lo para atualizar o container o instalar a aplicação, o comando  responsável por isso é o docker attach, conforme descrito abaixo:</p>


<p align="center"><img src="images/admin-docker/docker-attach.png"  width="350" height="37" align="middle"/></p>



<p align="justify">Observe que após a execução do comando o prompt do Sistema Operacional modificou, isso quer dizer que você passou a acessar o container.</p>


<p align="center"><img src="images/important.png"  width="240" height="64" align="middle"/></p>

<p align="justify">Para sair do container sem finalizar digite <b>ctrl + p + q</b>, se digitar exit o mesmo será finalizado</p>

### INICIANDO OU PARANDO CONTAINER

<p align="justify">Os comandos docker start ou docker stop são utilizado para iniciar ou parar a execução do container, devendo passar por parâmetros o nome do mesmo.</P>

### CONSULTANDO AS IMAGENS DISPONÍVEIS

<p align="justify">Caso o administrador do sistema necessite consultar as imagens que já foram baixadas no computador hospedeiro é necessário executar o comando docker images, conforme observado abaixo:</p>

<p align="center"><img src="images/admin-docker/docker-images.png"  width="600" height="61" align="middle"/></p>

### EXCLUSÃO DE CONTAINER

<p align="justify">Quando não existe mais necessidade de um container criado o administrador do sistema finaliza o mesmo com o docker stop, todavia os arquivos ainda ficam residindo no sistema, para apagar este container deve ser usado o comando docker rm nome_do_container, o mesmo só será aceito se o container já estiver desligado.</P>

### EXCLUSÃO DE IMAGEM

<p align="justify">O docker rmi é utilizado quando o administrador do container deseja remover as imagens baixadas no repositório local, na imagem abaixo apresenta o comando de remoção da imagem nginx.</p>

<p align="center"><img src="images/admin-docker/docker-rmi.png"  width="600" height="134" align="middle"/></p>

### VISUALIZAÇÃO DOS CONTAINER EM EXECUÇÃO

<p align="justify">Ao longo da administração de sistemas com docker se faz necessário visualizar os containers que estão em execução no momento, com este objetivo pode-se utilizar o comando docker ps, a figura abaixo apresenta um ambiente em que estão executando dois containers com o nome debian e ubuntu.</p>

<p align="center"><img src="images/admin-docker/docker-ps.png"  width="800" height="73" align="middle"/></p>

### CRIANDO UMA NOVA IMAGEM

<p align="justify">Ao criar um container o administrador do sistema pode instalar aplicações neste, e caso haja necessita salvar a imagens para reutilizar este container já preparado, para isso pode realizar o commit com o comando docker commit imagem_alterada nova_imagem, a imagem abaixo apresenta um exemplo, onde é criado uma nova imagem img-icev a partir do container icev, logo em seguida é exibido a lista de imagens do repositório local já com a nova criada</p>

<p align="center"><img src="images/admin-docker/docker-commit.png"  width="550" height="84" align="middle"/></p>

[Início](/README.md)
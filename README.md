# Website Rotaract Brasil

Link: https://rotaractbrasil.org.br/

## 🛠️ Pré-requisitos:
O site Rotaract Brasil utiliza um arquivo ``docker-compose`` para gerenciar e executar todos os containers do projeto. Para executá-lo, você precisará seguir os passos abaixo:
* instalar o [Docker](https://docs.docker.com/compose/install) no seu computador;
* adicioná-lo ao PATH do seu sistema.  
  
> [!TIP]
> Para saber se o seu sistema está reconhecendo o comando ``docker-compose``, execute a linha abaixo no terminal:
```
docker-compose --version
```
## ⚙️ Como usar:
É possível executar o arquivo ``docker-compose`` tanto pelo terminal quanto pelo aplicativo Docker. Independentemente do local escolhido, os comandos utilizados são os seguintes:
* Para ler o arquivo ``docker-compose.yml``, subir todos os containers especificados (wordpress, database e phpmyadmin) e liberar o terminal para outras aplicações;
```
docker-compose up -d
```

* Para interromper a execução dos containers.
```
docker-compose down
```  

> [!TIP]
> Ao subir os containers uma vez, o projeto será mapeado para os volumes especificados, então todas as atualizações feitas no código-fonte serão refletidas nos destinos fornecidos.

---
Os containers podem ser acessados na porta especificada para cada um deles.
* **Wordpress:** http://localhost:8000
* **PhpMyAdmin:** (interface do banco de dados):  http://localhost:8080  
  
> [!TIP]
> Caso ocorra conflito de porta, basta alterar os valores no arquivo ``docker-compose``.

---
Ao acessar o Wordpress, podem ser utilizadas as credenciais fornecidas no ``docker-compose``. 

Caso queira acessar diretamente as configurações do Wordpress, basta acessar o seguinte link: http://localhost:8000/wp-admin/

Se a instalação do Docker foi realizada corretamente e o arquivo ``docker-compose`` tiver sido executado, o tema do projeto já estará disponível. Basta acessar **Preferências > Tema** e ativar o tema **MDIO Rotaract Brasil**. 

---
Além disso, no painel do Wordpress, você deve configurar as páginas utilizadas na aplicação. Acesse **Páginas > Adicionar Página** e crie as seguintes páginas:


>  **_Título:_** listar-projetos  
> **_Template:_** listar-projetos  
> **_Slug:_** listar-projetos   


> **_Título:_** onde-estamos  
> **_Template:_** buscar-clube  
> **_Slug:_** onde-estamos  


>**_Título:_** projetos-destaque  
>**_Template:_** projetos-destaque  
>**_Slug:_**  projetos-destaque  

> [!TIP]
> Se a URL criada para cada página não tiver o seguinte formato: http://localhost:8000/nome-slug/, acesse **Settings > Permalink > Permalink structure** e selecione a opção **“Post Name”**. 

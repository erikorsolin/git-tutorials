
 # <img src="assets/logo.png" width="55" height="48">    Git Tutorials 

 Este repositório tem como objetivo oferecer um guia rápido dos comandos mais usados, para mais detalhes sobre a ferramenta, recomenda-se fortemente a leitura da [documentação oficial do Git](https://git-scm.com/doc)

## índice
[1. git config](#secao1)  
[2. git help](#secao2)  
[3. git init](#secao3)
[4. git clone](#secao4)
[5. git add](#secao5)


<a name="secao1"></a>
 ## 1. git config 
 O comando git config é usado para definir opções de configuração do Git em níveis local, global e de sistema, como nome de usuário e email. É útil para personalizar o comportamento do Git em diferentes ambientes.

```bash 
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

<a name="secao2"></a>
## 2. git help
O comando git help é utilizado para acessar a documentação e informações de ajuda sobre outros comandos do Git. Ao executar git help [comando], ele exibe uma página de manual detalhada sobre o comando específico, fornecendo descrições sobre o que ele faz, opções disponíveis e exemplos de uso.

```bash 
git help comando
```
<a name="secao3"></a>
## 3. git init
Caso  esteja iniciando o monitoramento de um projeto existente com Git, você precisa ir para o diretório do projeto e digitar

```bash 
git init
```
Caso você queira começar a controlar o versionamento dos arquivos existentes (diferente de um  diretório vazio), você provavelmente deve começar a monitorar esses  arquivos e fazer um commit inicial. Você pode realizar isso com poucos comandos

```bash 
touch .gitignore
git add .gitignore
git commit -m "Versão inicial do projeto"
```

<a name="secao4"></a>
## 4. git clone
O comando git clone é utilizado para criar uma cópia local de um repositório Git remoto. Ao executá-lo com a URL do repositório, ele baixa todos os dados, históricos e branches desse repositório para a sua máquina, permitindo que você trabalhe com todos os arquivos e histórico localmente.

```bash 
git clone url
```

<a name="secao5"></a>
## 5. git add
Para passar a monitorar um novo arquivo presente no projeto, use o comando

```bash 
git add nome_arquivo.ext
```

Para passar a monitorar todos os arquivos que ainda não estão sendo monitorados use o comando

```bash 
git add .
```

 # <img src="assets/logo.png" width="55" height="48">    Git Tutorials 

 Este repositório tem como objetivo oferecer um guia rápido dos comandos mais usados, para mais detalhes sobre a ferramenta, recomenda-se fortemente a leitura da [documentação oficial do Git](https://git-scm.com/doc)

## índice
[1. git config](#secao1)  
[2. git help](#secao2)  
[3. git init](#secao3)  
[4. git clone](#secao4)  
[5. git add](#secao5)  
[6. git status](#secao6)  
[7. git diff](#secao7)  
[8. git commit](#secao8)    
[9. git push](#secao9)  
[10. git pull](#secao10)  
[11. git branch](#secao11)  
[12. git checkout](#secao12)  
[13. git merge](#secao13) 


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
O comando git add é usado para adicionar mudanças nos arquivos do diretório de trabalho ao índice (staging area) do Git. Isso prepara os arquivos modificados para serem incluídos em um commit. Com esse comando, você pode especificar quais alterações ou arquivos deseja confirmar, permitindo que você divida suas mudanças em commits menores e mais gerenciáveis.

```bash 
git add nome_arquivo.ext
```

Para adicionar todos os arquivos modificados na staging area

```bash 
git add .
```

<a name="secao6"></a>
## 6. git status
O comando mostra em qual branch você se encontra, quais são os arquivos que estão sendo monitorados e não monitorados.

```bash 
git status
```

<a name="secao7"></a>
## 7. git diff
O comando git diff é utilizado para exibir as diferenças entre commits, branches, arquivos, e mais, no Git. Ele mostra as alterações que não foram ainda adicionadas ao stage (área de preparação) ou as diferenças entre o seu repositório local e o que está no repositório remoto, permitindo que você veja exatamente o que foi modificado.

```bash 
git diff 
```

<a name="secao8"></a>
## 8. git commit 
Armazena o conteúdo atual do índice em um novo commit, juntamente com uma mensagem de registro do usuário que descreve as mudanças. Se usa o commit depois de já ter feito o git add.

```bash 
git commit -m "mensagem" 
```
Refazendo commit quando esquecer de adicionar algum arquivo no Stage:

```bash 
git commit -m "mensagem" --amend
```
O amend é destrutivo e só deve ser utilizado antes do commit ter sido enviado ao servidor remoto.


<a name="secao9"></a>
## 9. git push
Envia o(s) commit(s) para o servidor remoto.

```bash 
git push
```

<a name="secao10"></a>
## 10. git pull
Puxa o(s) commit(s) do servidor remoto.

```bash 
git pull
```

<a name="secao11"></a>
## 11. git branch
Cria uma ramificação (branch) a partir da branch atual.

```bash 
git branch nome-da-branch
```

Para deletar uma branch, use o comando

```bash 
git branch -d nome-da-branch
```

Para excluir a branch no servidor remoto, use o comando

```bash 
git push origin --delete nome-da-branch
```

<a name="secao12"></a>
## 12. git checkout
Muda para a branch especificada.

```bash 
git checkout nome-da-branch
```
É possível criar uma branch a partir da atual a imediatamente mudar para ela com o comando

```bash 
git checkout -b nome-da-branch
```

<a name="secao13"></a>
## 13. git merge
Integra alterações de uma branch em outra.
1. Mudar para a branch destino

```bash 
git checkout nome-da-branch-destino
```

2. Executar o merge

```bash 
git merge nome-da-branch-origem
```

Este comando tentará mesclar as alterações da branch `nome-da-branch-origem` na branch `nome-da-branch-destino`. Se não houver conflitos, o Git criará um commit de merge, a menos que o merge possa ser resolvido via "fast-forward".

**fast-forward:** Ocorre quando a branch destino não teve novos commits desde que a branch a ser mesclada foi criada dela. O Git simplesmente move o ponteiro HEAD da branch destino para o ponteiro da branch a ser mesclada. 

**Merge commit**: Se ambas as branches tiveram alterações, o Git criará um commit de merge. Este commit terá dois pais, indicando que ele mescla duas linhas de desenvolvimento.

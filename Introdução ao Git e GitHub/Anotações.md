# Introdução ao Git e Github

Class: Git
Created: June 3, 2022 10:07 AM
Reviewed: No
Type: Módulo 1

# 1. Introdução ao Git

> **Git é um sistema de controle** de versão desenvolvido por Linus Torvalds.
> 
> 
> Isso significa que **qualquer desenvolvedor numa equipe pode gerenciar o código-fonte e seu histórico de mudanças** 
> 
> usando ferramentas de linha de comandos de Git – desde que tenha sido concedido o acesso para isso, é claro.
> 

## Benefícios do Git e Github

- Controle de versão
- Armazenamento em nuvem
- Trabalho em equipe
- Aperfeiçoamento de código
- Reconhecimento

# 2. Navegação no terminal e Instalação do Git

## Comandos básicos para bom desempenho no terminal

### O que será aprendido?

- Mudar de pastas
- Listar as pastas
- Criar pastas/arquivos
- Deletar pastas/arquivos

### Comandos

- **dir**: lista todos os diretórios existentes em uma pasta.
- **cd**: serve para navegar entre pastas pelo prompt.
    - **cd /**: navega para local específico.
- **cls**: limpa o prompt.
- **tab**: auto-completa palavra.
- **mkdir**: cria uma pasta (”make directory”).
- **del**: deleta arquivo dentro de pasta.
- **rmdir**: deleta pasta (”remove directory”).

# 3. Como o Git funciona

### **Secure Hash Algorithm** (SHA).

> É um **conjunto de funções hash criptográficas** projetadas pela NSA
> 
> 
> (Agência de Segurança Nacional dos EUA).
> 
- A **encriptação gera um conjunto de caracteres identificador** de 40 dígitos único.
- O SHA1 é uma **forma curta de representar um arquivo**.

### Exemplo

- Conteúdo foi alterado na segunda vez. Na terceira, foi igual a primeira.

![Exemplo de encriptação.](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled.png)

Exemplo de encriptação.

## Objetos internos do Git

### Objetos básicos do Git

- **Blob**: A partir do conteúdo de um arquivo, ele **gera um hash** que será armazenado em algum lugar endereçável.
- **Tree**: Resolve o problema de armazenar o nome de arquivo e também permite armazenar de forma conjunta um grupo de arquivos.
- **Commit**: É o hash de toda a informação.

![Exemplo de trees e blobs.](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%201.png)

Exemplo de trees e blobs.

> Quando você executa o comando ***git add**,* o git bate uma foto (snapshot) do working directory e a armazena em sua memória interna,
> 
> 
> quando você executar o comando ***git commit*** o seguinte objeto de commit num pseudo código será gerado:
> 

```jsx
sha1(
 commit message => feature commit”
 committer => Lilian Lima < lilian.lima@mail.com>
 commit date => Sat Jun 8 09:15:59 2019 +0100
 author => Lilian Lima < lilian.lima@mail.com>
 author date => Sat Jun 8 09:15:59 2019 +0100
 tree => 508222e4b5ba555711173ff140a6263bef867166
 parents => [d0957cc8c91520eedcd3807baa96170020812f0e]
)
```

### Conteúdos explicativos

- [**https://deviniciative.wordpress.com/2019/06/28/a-anatomia-de-um-commit-no-git/**](https://deviniciative.wordpress.com/2019/06/28/a-anatomia-de-um-commit-no-git/)
- [**https://git-scm.com/book/pt-br/v2/Funcionamento-Interno-do-Git-Objetos-do-Git**](https://git-scm.com/book/pt-br/v2/Funcionamento-Interno-do-Git-Objetos-do-Git)

## Chaves SSH e Tokens

### Chave SSH

> O **SSH (Secure Shell)**, também conhecido como Secure Socket Shell, é um **protocolo que permite a conexão**
> 
> 
> **com servidores remotos**, **de forma criptografada e mais segura**, usando um par de chaves RSA.
> 
> Este método **consiste na criação de duas chaves**, **uma pública** que deve ser instalada nos servidores remotos, 
> 
> **e a outra chave privada** que fica salva em um local seguro.
> 

### Gerando chave SSH

![Passo a passo da geração de chave](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%202.png)

Passo a passo da geração de chave

### Instruções

- [**https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent**](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Token de Acesso Pessoal

> Os tokens de acesso pessoal (PATs) são uma **alternativa para o uso de senhas para autenticação no GitHub**
> 
> 
> ao usar a API do GitHub ou a linha de comando.
> 

### Instruções

- [**https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token**](https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

### Dicas

- **CRTL + L**: limpa o prompt do git bash.
- Git Bash é o terminal extendido para otimizar o uso do Git.

# 4. Iniciando o Git e criando um commit

### Comandos

- **git init**
- **git add**
- **git commit**

### Passos

1. Criando Repositório

![Criando repositorio livro-receitas](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%203.png)

Criando repositorio livro-receitas

# 5. Ciclo de vida dos arquivos no Git

![Ciclo de vida de um arquivo](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%204.png)

Ciclo de vida de um arquivo

### Repositórios

![Untitled](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%205.png)

### Comandos

- **git status**: ajuda os desenvolvedores a rastrear suas alterações não confirmadas e
  
    a entender como seus arquivos de projeto estão sendo rastreados.
    

![Etapas em que cada comando é utilizado](Introduc%CC%A7a%CC%83o%20ao%20Git%20e%20Github%20e7c08be81c80497b8ca3e078ab2aec6d/Untitled%206.png)

Etapas em que cada comando é utilizado

# 6. Introdução ao Github

### Criando Repositório

- Passo a passo:
    - [**https://docs.github.com/pt/repositories/creating-and-managing-repositories/creating-a-new-repository**](https://docs.github.com/pt/repositories/creating-and-managing-repositories/creating-a-new-repository)

# 7. Resolvendo Conflitos

### Conflito de Merge

> São **causados por alterações concorrentes na linha**, como quando as pessoas fazem alterações diferentes
> 
> 
> na mesma linha do mesmo arquivo em diferentes branches no seu repositório Git.
> 
- [**https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github**](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)

### Git Pull

> O comando **git pull** é usado para **buscar e baixar conteúdo de repositórios remotos e fazer a atualização**
> 
> 
> imediata ao repositório local para que os conteúdos sejam iguais.
> 

### Git Clone

> O **git clone** é **usado para copiar um repositório Git existente em um novo diretório local**.
> 
> 
> A ação git clone criará um novo diretório local para o repositório, copiará todo o conteúdo do repositório especificado,
> 
> criará as ramificações rastreadas remotas e fará o check-out de uma ramificação inicial localmente. 
> 
> Por padrão, o clone criará uma referência ao repositório remoto chamado origin.
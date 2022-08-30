# Comandos básicos no terminal

**change directory**
L: ```cd /```
W: ```cd /```

**previous page**
L: ```cd ..```
W: ```cd ..```

**Listar as pastas**
L: ```dir```
W: ```ls```

**Criar pastas/arquivos**
W & L: ```mkdir```

**Deletar pastas/arquivos**
L: ```rm -rf nome_da_pasta```
W: ```del``` //(deleta arquivos, caso indique a pasta, irá deletar arquivos da pasta
```rmdir nome_da_pasta /s /q```

**Outros**
**limpar terminal**
L: ```clear``` ou Ctrl+L
W: ```cls``` //clear screen

**auto completar**
W & L: TAB

# Entendendo GIT por baixo dos panos

## SHA1

A sigla SHA significa Secure Hash Algorithm, um conjunto de funções hash criptográficas projetadas pela NSA (National Security Agency) dos EUA
Gera um conjunto de caracteres de 40 dígitos único para o arquivo

## Objetos fundamentais

Responsável por versionamento de códigos

### Blobs

Carrega o tipo, tamanho do arquivo, tamanho da string, “\0”, etc

### Trees

Armazena os blobs: \0, blob, SHA1 e nome do arquivo. Aponta também para outras trees, para identificar os diretórios de onde está armazenado

### Commits

Aponta para uma tree, para outro commit, autor, mensagem e timestamp (data e hora de criação) 

### Sistema distribuído e Segurança

As versões geradas são super confiáveis, pela estrutura acima explicada de criptografia e “versionamentos”  

# Primeiros comandos com GIT

## Criando um user

```git config --global user.name "jondoe"``` //deve ser o mesmo do github
```git config --global user.email "jondoe@gmail.com"```

## Criando um repósitório

```git init```
Cria uma pasta ./git e inicia o conceito de repositório 

## Criando um commit

Um Commit é um pacote de alterações feitas no repositório. Cada commit possui arquivos alterados, autor e uma mensagem de resumo.

1. Depois de criar o arquivo README.md no repositório local, por exemplo, ele ficará com o status de "untracked".
2. Para adicionar o arquivo a um Commit, usar o comando  

```git add README.md```
3. Agora o arquivo está pronto para ser empacotado em um commit. Escrever o comando de commit incluindo uma mensagem que explique o que sua alteração faz no repositório:

```git commit -m "Adiciona arquivo README.md"```

# Enviando os Commits para o GitHub

Já criado um repositório localmente, para subir o mesmo ao GitHub Primeiro devemos configurar qual o repositório remoto. Executar usando a URL do seu repositório:

```git remote add origin https://github.com/shotonguren/desafio_github_primeiro_repositorio.git```

E para enviar os arquivos do repositório

```git push -u origin main```

Colocar usuário e senha (GitHub) ou token

## Trazendo um repositório remoto para local

```git pull```

## Baixando outros repositórios

```git clone https://github.com/shotonguren/desafio_github_primeiro_repositorio.git```

# Curso-Git
Curso de versionamento de código com Git
***

## Introdução ao Git

**Git:** Software de Controle de Versão (VCS)

**Principais vantagens:**

- Controle de histórico: Acesso a versões anteriores do código.
- Ramificação do projeto: Possibilidade de separar diferentes partes do mesmo código.

## Instalação do Git

Você pode instalar o Git em seu computador a partir do [site oficial](https://git-scm.com/downloads).

## Conceitos Básicos

### Comandos Git
1. - **git clone:** Git clone é uma comando para baixar o código-fonte existente de um repositório remoto 
- Clone por HTTPS
```C:\Curso-Git> git clone https://gitlab.com/11joao44/nome_projeto.git```
- Clone por SSH
```C:\Curso-Git> git clone git@gitlab.com:11joao44/nome_projeto.git```
os dois metodos fazem a mesma função, mas o SSH é Criptografado sendo mais seguro.

2. - **Git branch:** Branches (Ramificações, em português) 
     Trabalhar em paralelo no mesmo projeto simultaneamente.
     Com git branch podemos criar, listar e excluir as branches.

 - Criar branch
```C:\Curso-Git> git branch nome_branch```
esse comando cria uma branch no seu repositorio-local e estará apenas na sua maquina

- Para enviar para o repositorio-remoto precisar usar o comando push
```C:\Curso-Git> git push -u  https://gitlab.com/11joao44/nome_projeto.git nome_branch```

 - Ver todas a branch 
```C:\Curso-Git> git branch```

 - Excluir branch 
```C:\Curso-Git> git branch -d nome_branch```

3. **Git checkout:** Ele é usado para navegar entre branches. 

    ```bash
    Comando para verificar as branch e visualizando a atual
    C:\Curso-Git> git branch
      developer
      * main

    Comando para mudar para outra branch
    C:\Curso-Git> git checkout developer
      Mudou para branch 'developer'

    Comando para verificar as branch e visualizando a atual
    C:\Users\11joa\OneDrive\Documentos\GitHub\Curso-Git> git branch
      * developer
      main
    ```

4. **Git status:** git status mostra informações sobre a branch atual.
   ```bash 
   C:\Curso-Git> git status
    Mudanças não preparadas para commit:
    (use "git add ." para atualizar tudo que será confirmado)
    (use "git restore <file>..." para descartar alterações no diretório de trabalho)
            modificado: README.md - no terminal ficará em vermelho

   Comando para adicionar todas as alterações
   C:\Curso-Git> git add .
   C:\Curso-Git> git status
    Mudanças pronta commit:
    (use "git restore --staged <file>..." para desestabilizar)
            modificado: README.md - no terminal ficará em verde
   ```
5. **Git add:** git add serve para incluir as alterações de um ou vários arquivos em nosso próximo commit.

  - Adicionar um único arquivo
  ```C:\Curso-Git> git add nome_arquivo```

  - Adicionar todos os arquivos
  ```C:\Curso-Git> git add -A```

  - Adicionar todos os arquivos menos os excluidos 
  ```C:\Curso-Git> git add .```

  **O comando git add não altera o repositório. As alterações não são salvas até que se use o git commit.**

6. **Git commit:** Comando para adicioanr e registrar as alterações no seu repositório. 

    ```C:\Curso-Git> git commit -m "Sua mensagem de commit aqui"```

    **Importante: git commit salva suas alterações apenas no repositorio-local.**

7. **Git push:** Comando para enviar suas alterações ao servidor remoto. 
   Git push faz o upload dos seus commits e alterações no repositório remoto. 

    ```C:\Curso-Git> git push  https://gitlab.com/11joao44/nome_projeto.git nome_branch```

8. **Git pull:** O comando git pull é usado para obter as atualizações de um repositório remoto. 

    ```C:\Curso-Git> git pull  https://gitlab.com/11joao44/nome_projeto.git```

    **ele recebe as atualizações do repositório remoto e aplica imediatamente as alterações mais recentes no seu repositorio-local**

9. **Git revert:** O git revert é usado para desfazer um commit anterior
                   e criando um novo commit que reverte as alterações 

    ```C:\Curso-Git> git revert commit-hash``` **O hash (identificador único) do commit**

    **Para ver nosso histórico de commits, primeiro, precisamos usar git log -- oneline**

10. **Git merge:** Git merge para unir uma branch com outra.

    ```C:\Curso-Git> git merge branch_principal```

    **combinar as alterações de uma branch em outra, criando um novo commit de mesclagem que representa a união das mudanças das branches envolvidas*
### Alterações no Código
- **Changes:** Indica que houve modificações no código.
- **Fetch origin:** Verifica se o código teve alguma modificação feita por outro desenvolvedor.
- **Pull:** Obtém as modificações que outro desenvolvedor fez e as incorpora ao seu código.

### Tratamento de Erros

#### Erro de Histórico

Ao realizar um `git pull`, você pode se deparar com o erro:

warning: redirecting to https://gitlab.com/11joao44/nome_projeto/
fatal: refusing to merge unrelated histories


Solução: Utilize `git pull --allow-unrelated-histories` para permitir a mesclagem de histórias não relacionadas.

#### Conflitos de Mesclagem (Merge)

Se ocorrerem conflitos durante a mesclagem, você pode resolver manualmente da seguinte maneira:

1. Abra o arquivo `index.html` em um editor de texto.
2. Encontre as áreas de conflito marcadas como:

```plaintext
<<<<<<< HEAD
Conteúdo da sua branch local
=======
Conteúdo da branch remota
>>>>>>> commit-hash
```

Solução: Utilize `git pull --allow-unrelated-histories` para permitir a mesclagem de histórias não relacionadas.

#### Conflitos de Mesclagem (Merge)

Se ocorrerem conflitos durante a mesclagem, você pode resolver manualmente da seguinte maneira:

1. Abra o arquivo `index.html` em um editor de texto.
2. Encontre as áreas de conflito marcadas como:

```plaintext
<<<<<<< HEAD
Conteúdo da sua branch local
=======
Conteúdo da branch remota
>>>>>>> commit-hash
```

Edite o arquivo para escolher as partes do código que deseja manter, removendo as marcações.
Salve o arquivo.
Adicione o arquivo resolvido: git add index.html
Cometa as alterações: git commit -m "Resolva conflitos no arquivo index.html"
Continue com o pull: git pull

# Issues
Use as "Issues" para tirar dúvidas, relatar problemas não resolvidos ou compartilhar soluções.

# Markdown
Markdown: Linguagem de marcação leve para formatação de texto.
Usada nesse arquivo.

# Branch/Ramificação
As branches são usadas para desenvolver funcionalidades isoladamente do código principal.
Exemplo de criação de uma nova branch e alternância para ela:
# Crie uma nova branch chamada "minha-feature"
git checkout -b minha-feature

# Faça alterações e commits na nova branch

# Quando estiver pronto para mesclar na branch principal (geralmente "main"):
git checkout main
git merge minha-feature

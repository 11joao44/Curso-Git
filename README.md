# Curso-Git
Curso de versionamento de código com Git
## Introdução ao Git

**Git:** Software de Controle de Versão (VCS)

**Principais vantagens:**

- Controle de histórico: Acesso a versões anteriores do código.
- Ramificação do projeto: Possibilidade de separar diferentes partes do mesmo código.

## Instalação do Git

Você pode instalar o Git em seu computador a partir do [site oficial](https://git-scm.com/downloads).

## Comandos Git
### Git clone:  
> **Git clone é uma comando para baixar o código-fonte existente de um repositório remoto** 

1. Clone por HTTPS
```bash
C:\Curso-Git> git clone https://gitlab.com/11joao44/nome_projeto.git 
```

2. Clone por SSH
```bash
C:\Curso-Git> git clone git@gitlab.com:11joao44/nome_projeto.git
```  
- `os dois metodos fazem a mesma função, mas o SSH é Criptografado sendo mais seguro.`
***

### Git branch:  
> **Branches (Ramificações, em português) Trabalhar em paralelo no mesmo projeto simultaneamente.**
> 
> **Com git branch > podemos criar, listar e excluir as branches.**

1. Criar branch
```bash
C:\Curso-Git> git branch nome_branch
```
- esse comando cria uma branch no seu repositorio-local e estará apenas na sua maquina

2. Ver todas a branch
```bash
C:\Curso-Git> git branch
```  

3. Excluir branch 
```bash
C:\Curso-Git> git branch -d nome_branch
```
***

### Git checkout:  
> **Ele é usado para navegar entre branches.**
  
1. Comando para verificar as branch e visualizando a atual  
```bash
C:\Curso-Git> git branch
    developer
    '* main'
```  

2. Comando para mudar para outra branch  
```bash
    C:\Curso-Git> git checkout developer
      Mudou para branch 'developer'
```  

3. Comando para verificar as branch e visualizando a atual
```bash
    C:\Curso-Git> git branch
      '* developer'
      main
``` 
***

### Git status:  
> **git status mostra informações sobre a branch atual.**

1. Exemplo
```bash 
C:\Curso-Git> git status
    'Mudanças não preparadas para commit:'
    (use "git add ." para atualizar tudo que será confirmado)
    (use "git restore <file>" para descartar alterações no diretório de trabalho)
            'modificado:' README.md - no terminal ficará em vermelho
```

2. Comando para adicionar todas as alterações
```bash
C:\Curso-Git> git add .
```

3. Olhando as informações depois do 'git add'
```bash
C:\Curso-Git> git status
    Mudanças pronta para commit:
    (use "git restore --staged <file>..." para desestabilizar)
        modificado: README.md - no terminal ficará em verde
```
***
### Git add 
> **git add serve para incluir as alterações de um ou vários arquivos em nosso próximo commit.**

1. Adicionar um único arquivo
```bash
C:\Curso-Git> git add nome_arquivo
```

2. Adicionar todos os arquivos
```bash
C:\Curso-Git> git add -A
```

3. Adicionar todos os arquivos menos os excluidos 
```bash
C:\Curso-Git> git add .
```

**O comando git add não altera o repositório. As alterações não são salvas até que se use o git commit.**
***

### Git commit:
> **Comando para adicioanr e registrar as alterações no seu repositório.**

```bash 
C:\Curso-Git> git commit -m "Sua mensagem de commit aqui"
```

**Importante: git commit salva suas alterações apenas no repositorio-local.**
***

### Git push:
> **Comando para enviar suas alterações ao servidor remoto.**
> **Git push faz o upload dos seus commits e alterações no repositório remoto.**

```bash
C:\Curso-Git> git push  https://gitlab.com/11joao44/nome_projeto.git nome_branch
```
***

### Git pull:
> **O comando git pull é usado para obter as atualizações de um repositório remoto.** 

```bash 
C:\Curso-Git> git pull  https://gitlab.com/11joao44/nome_projeto.git
```

**ele recebe as atualizações do repositório remoto e aplica imediatamente as alterações mais recentes no seu repositorio-local**
***

### Git revert:
> **O git revert é usado para desfazer um commit anterior e criando um novo commit que reverte as alterações.**

```bash
C:\Curso-Git> git revert commit-hash
``` 
**O hash (identificador único) do commit**

**Para ver nosso histórico de commits, primeiro, precisamos usar git log -- oneline**
***

### Git merge:
> **Git merge para unir uma branch com outra.**

```bash
C:\Curso-Git> git merge branch_principal
```

**combinar as alterações de uma branch em outra, criando um novo commit de mesclagem que representa a união das mudanças das branches envolvidas**
***

### Lista dos comandos

1. `git init`: Inicializa um novo repositório Git.
2. `git clone`: Clona um repositório Git existente para o seu diretório local.
3. `git add`: Adiciona alterações no diretório de trabalho ao índice (staging area).
4. `git commit`: Cria um novo commit com as alterações no índice, adicionando uma mensagem de commit.
5. `git status`: Exibe o status atual do seu diretório de trabalho, mostrando as alterações pendentes.
6. `git log`: Exibe o histórico de commits do repositório.
7. `git diff`: Mostra as diferenças entre o diretório de trabalho e o último commit.
8. `git branch`: Lista todas as branches no repositório e destaca a branch atual.
9. `git checkout`: Altera a branch atual ou restaura arquivos do histórico.
10. `git merge`: Mescla as alterações de uma branch em outra.
11. `git pull`: Obtém as alterações do repositório remoto e as mescla na branch atual.
12. `git push`: Envia os commits locais para o repositório remoto.
13. `git fetch`: Obtém as alterações do repositório remoto, mas não as mescla automaticamente.
14. `git remote`: Gerencia repositórios remotos.
15. `git stash`: Salva alterações não commitadas em uma pilha temporária.
16. `git tag`: Cria, lista ou verifica tags.
17. `git reset`: Volta o estado do repositório para um commit anterior.
18. `git rebase`: Reorganiza commits para uma base comum.
19. `git blame`: Mostra quem fez cada alteração em um arquivo.
20. `git grep`: Pesquisa em arquivos do repositório.
21. `git rm`: Remove arquivos do repositório.
22. `git config`: Configura opções do Git.
23. `git show`: Exibe informações detalhadas sobre um commit.
24. `git remote add`: Adiciona um repositório remoto.
25. `git remote remove`: Remove um repositório remoto.
26. `git remote -v`: Exibe repositórios remotos configurados.
27. `git checkout -b`: Cria e muda para uma nova branch.
28. `git log --graph`: Exibe o histórico de commits em um formato de árvore gráfica.
29. `git cherry-pick`: Aplica um commit específico em uma branch.
30. `git bisect`: Ajuda a encontrar um commit problemático usando uma busca binária.
31. `git show-branch`: Exibe um resumo das branches.
32. `git rebase -i`: Permite a edição interativa de commits durante um rebase.
33. `git reflog`: Exibe um registro de referências de branches recentes.
34. `git rev-parse`: Traduz ou analisa objetos Git.
35. `git clean`: Remove arquivos não rastreados no diretório de trabalho.
36. `git commit --amend`: Adiciona mudanças ao commit anterior.

### Tratamento de Erros

#### Erro de Histórico
- Ao realizar um `git pull`, você pode se deparar com o erro:

```
warning: redirecting to https://gitlab.com/11joao44/nome_projeto/
fatal: refusing to merge unrelated histories
```

**Solução:** Utilize ```git pull --allow-unrelated-histories``` para permitir a mesclagem de histórias não relacionadas.

### Conflitos de Mesclagem (Merge)

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

**Solução:** Utilize novamente o `git pull --allow-unrelated-histories` para permitir a mesclagem de histórias não relacionadas.

Edite o arquivo para escolher as partes do código que deseja manter, 
removendo as marcações, Salve o arquivo.

Adicione o arquivo resolvido: git add index.html

Cometa as alterações: git commit -m "Resolva conflitos no arquivo index.html"
Continue com o pull: `git pull`

# Issues
Use as "Issues" para tirar dúvidas, relatar problemas não resolvidos ou compartilhar soluções.

# Markdown
Markdown: Linguagem de marcação leve para formatação de texto.
Usada nesse arquivo.

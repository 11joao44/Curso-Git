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

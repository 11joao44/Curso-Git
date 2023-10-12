# Curso-Git
 Curso de versionamento de código com Git

 -------- Curso GIT ---------
Git: Software de Controle de Versão - VCS

Principais vantagens
► Controle de histórico - acessar versões anteriores do código
► Ramificação do projeto - separar em parte do memso arquivo

Instalar Git no computador 
Link: https://git-scm.com/downloads

Changes: Significa houve mudanças no código.
Fecth origin: Verificar se o código teve alguma modificação de outro dev.
Pull: Pegar as modificações que o outro dev fez e carrega no meu código.

► Tratamento de erro

Erro de historico: 
warning: redirecting to https://gitlab.com/11joao44/nome_projeto/
fatal: refusing to merge unrelated histories

Solução: git pull --allow-unrelated-histories


Erro de merging:
warning: redirecting to https://gitlab.com/11joao44/nome_proejto/
Auto-merging index.html
CONFLICT (add/add): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

Sobre: 
O comando git pull --allow-unrelated-histories 
resultou em um conflito de merge no arquivo index.html. 
Isso ocorreu porque o Git está tentando mesclar duas linhagens de histórico 
que não têm um ancestral comum.

Solução: Você precisa resolver esse conflito manualmente. 

A seção entre <<<<<<< HEAD e ======= representa as alterações da sua branch local. #Verde
A seção entre ======= e >>>>>>> commit-hash representa as alterações da branch remota. #Roxa
resolver os conflitos, remova as marcações <<<<<<< HEAD, =======, >>>>>>> commit-hash
e deixe o código como você deseja que ele fique após a mesclagem.

git add index.html
git commit -m "Resolva conflitos no arquivo index.html"
git pull
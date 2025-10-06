# Git de Bolso: Guia de Git e GitHub

## Configuração Inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git config --list
````

* `git config --global user.name "Seu Nome"` → Define o nome que será gravado em cada commit que você fizer.
* `git config --global user.email "seuemail@exemplo.com"` → Define o e-mail vinculado aos commits (de preferência o mesmo do GitHub).
* `git config --list` → Lista todas as configurações feitas no Git.

**Definição**: essa configuração inicial serve para identificar o autor das alterações no histórico do projeto.

## Criando e Inicializando Repositórios

```bash
git init
git clone <url>
```

* `git init` → Transforma uma pasta comum em um repositório Git.
* `git clone <url>` → Faz o download de um repositório existente do GitHub (ou outro servidor) para o seu computador.

**Definição**: repositórios são como pastas com histórico, onde tudo o que você faz fica registrado. Você pode criar um do zero (`git init`) ou copiar um que já existe (`git clone`).

## Controle de Arquivos

```bash
git status
git add <arquivo>
git add .
git rm <arquivo>
```

* `git status` → Mostra o que foi alterado, o que já está preparado e o que ainda não está.
* `git add <arquivo>` → Seleciona arquivos específicos para o próximo commit.
* `git add .` → Seleciona todos os arquivos modificados.
* `git rm <arquivo>` → Remove um arquivo do repositório (também registra isso no histórico).

**Definição**: esses comandos controlam quais arquivos entram ou saem do próximo registro no histórico (commit).

## Commits

```bash
git commit -m "Mensagem"
git log
git log --oneline
```

* `git commit -m "Mensagem"` → Cria um commit com as alterações que você preparou.
* `git log` → Mostra todos os commits já feitos, em ordem cronológica.
* `git log --oneline` → Mostra o histórico resumido (cada commit em uma linha).

**Definição**: commits são como fotos do seu projeto em um momento específico. Eles guardam o estado do código e a mensagem explica o que foi feito.

## Branches

```bash
git branch
git branch <nome>
git checkout <nome>
git checkout -b <nome>
git merge <nome>
git branch -d <nome>
```

* `git branch` → Lista todas as branches do repositório.
* `git branch <nome>` → Cria uma nova branch.
* `git checkout <nome>` → Troca para uma branch existente.
* `git checkout -b <nome>` → Cria e já entra em uma nova branch.
* `git merge <nome>` → Mescla o conteúdo de uma branch na atual.
* `git branch -d <nome>` → Apaga uma branch que não é mais necessária.

**Definição**: uma branch é como uma linha de tempo separada do projeto. Ideal para desenvolver novas funcionalidades sem afetar a versão principal.

## Sincronização com GitHub

```bash
git remote add origin <url>
git remote -v
git push -u origin main
git push
git pull
git fetch
```

* `git remote add origin <url>` → Conecta seu repositório local a um remoto (como o GitHub).
* `git remote -v` → Mostra os repositórios remotos configurados.
* `git push -u origin main` → Envia a branch main para o GitHub (primeira vez).
* `git push` → Envia os commits locais para o GitHub.
* `git pull` → Baixa e aplica as alterações do GitHub no repositório local.
* `git fetch` → Apenas baixa as alterações do remoto, sem aplicar ainda.

**Definição**: esses comandos servem para manter o repositório local e o do GitHub sincronizados, permitindo colaboração e backup.

## Stash (Progresso Temporário)

```bash
git stash
git stash list
git stash pop
```

* `git stash` → Guarda alterações temporariamente (sem commit).
* `git stash list` → Lista os stashes salvos.
* `git stash pop` → Restaura as alterações guardadas.

**Definição**: o stash funciona como uma caixa de rascunho: você guarda seu trabalho inacabado para poder voltar a ele depois.

## Reverter Alterações

```bash
git checkout -- <arquivo>
git reset --hard HEAD
git revert <hash>
```

* `git checkout -- <arquivo>` → Restaura um arquivo para a última versão commitada.
* `git reset --hard HEAD` → Descarta todas as alterações não commitadas.
* `git revert <hash>` → Cria um commit que desfaz as alterações de um commit anterior.

**Definição**: esses comandos permitem corrigir erros, restaurar arquivos e até voltar o projeto para um estado anterior. `hash` é o identificador único de um commit, composto por 40 caracteres.

## Boas Práticas

* Faça commits pequenos, claros e frequentes.
* Use mensagens descritivas e no imperativo (ex.: "Adiciona função X").
* Crie branches para funcionalidades ou correções.
* Mantenha a main sempre estável.
* Sempre use `git pull` antes de começar a trabalhar.

---

## Fontes

* [Git e GitHub: Compartilhando e Colaborando em Projetos](https://www.alura.com.br/curso-online-git-github-compartilhando-colaborando-projetos?srsltid=AfmBOoqZ0iUtysWMW-bQfvwc47vhDtBmW6kJQonOVT1rQ-T9Tf62_LkB) - Alura
* [Documentação oficial do Git](https://git-scm.com/docs)

Última atualização: Outubro/2025  










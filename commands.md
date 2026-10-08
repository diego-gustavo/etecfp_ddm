# Passo a passo de como desenvolver em computadores "amnésicos"

## Configurações locais

### Antes de tudo, configure suas credenciais na nova máquina
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

## Preparando o repositório local

### Iniciar o repositório local (caso não tenha feito via 'git clone')
git init

### Adicionar o repositório remoto (origin)
git remote add origin https://github.com/diego-gustavo/etecfp_ddm.git

### Renomear a branch padrão para main (recomendado usar -M para forçar se necessário)
git branch -M main

## Fluxo de desenvolvimento

### Toda aula ou projeto novo, criar e já trocar para a nova branch
git checkout -b nome-da-branch

### Após fazer as alterações no código, adicionar os arquivos ao stage
git add .

### Salvar o estado (commit) com uma mensagem descritiva
git commit -m "Sua mensagem de commit aqui"

### Enviar as modificações para o GitHub (isso permite criar o Pull Request na plataforma)
git push -u origin nome-da-branch

## Fluxo de merge

### Caso queira mergear a branch que estamos trabalhando para dentro da main:

#### 1. Voltar para a branch principal
git checkout main

#### 2. Baixar atualizações que possam ter ocorrido no repositório remoto
git pull origin main

#### 3. Unir (merge) a branch de trabalho com a main
git merge nome-da-branch

#### 4. Enviar a branch main atualizada para o GitHub
git push origin main
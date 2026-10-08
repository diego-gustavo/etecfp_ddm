# Passo a passo de como desenvolver em computadores "amnésicos"

## Configurações locais

### Antes de tudo, configure suas credenciais na nova máquina
```cmd
git config --global user.email "your.email@example.com"
```
```cmd
git config --global user.name "Your Name"
```
## Preparando o repositório local

### Iniciar o repositório local (caso não tenha feito via 'git clone')
```cmd
git init
```

### Adicionar o repositório remoto (origin)
```cmd
git remote add origin https://github.com/diego-gustavo/etecfp_ddm.git
```

### Renomear a branch padrão para main (recomendado usar -M para forçar se necessário)
```cmd
git branch -M main
```

## Fluxo de desenvolvimento

### Toda aula ou projeto novo, criar e já trocar para a nova branch
```cmd
git checkout -b nome-da-branch
```

### Após fazer as alterações no código, adicionar os arquivos ao stage
```cmd
git add .
```

### Salvar o estado (commit) com uma mensagem descritiva
```cmd
git commit -m "feat: adição - fix: correção"
```

### Enviar as modificações para o GitHub (isso permite criar o Pull Request na plataforma)
```cmd
git push -u origin nome-da-branch
```

## Fluxo de merge

### Caso queira mergear a branch que estamos trabalhando para dentro da main:

#### 1. Voltar para a branch principal
```cmd
git checkout main
```

#### 2. Baixar atualizações que possam ter ocorrido no repositório remoto
```cmd
git pull origin main
```

#### 3. Unir (merge) a branch de trabalho com a main
```cmd
git merge nome-da-branch
```

#### 4. Enviar a branch main atualizada para o GitHub
```cmd
git push origin main
```

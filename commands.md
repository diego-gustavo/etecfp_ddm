// antes de tudo, configure suas credenciais
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

// caso precise, adicione o origin
git remote add origin https://github.com/diego-gustavo/etecfp_ddm.git
git branch -m main
git push -u origin main --force


// toda aula ou projeto novo, trocar de branch antes de começar qualquer coisa
git checkout branch-name

// para enviar as modificações para o github, isso vai criar uma pull request no github
git push [completar]

// caso queira mergear a branch main e a que estamos trabalhando, usar:
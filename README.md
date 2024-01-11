### Olá, sejam bem-vindo no meu perfil! 👋
### 🍂 Vou compartilhar com você um pouquinho sobre mim! ♥
<!--### É um prazer em receber você no meu perfil-->
<!-- comentários
**JessicaCastro88/jessicacastro88** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile. -->

- 🔭 Atualmente estou trabalhando como Engenheiro de dados
- 🌱 Estou aperfeiçoando meus conhecimentos como Engenheiro de dados e estudando inglês
- ⚡ Curiosidade sobre mim é que sou apaixonada com ovo mas não surporte o "Gosto de ovo cru" 
- 👩‍💻 Estou desenvolvendo um projeto pessoal e logo mais disponibilizo aqui para vocês aqui ♥
- 🤝 Amo me comunicar e ajudar aqueles que precisam!

<!-- comentários -->

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  

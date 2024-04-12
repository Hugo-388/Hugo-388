<body>
<h1 align="center">Bienvenue sur mon profil GitHub 👋</h1>


- 📚 Première année BTS SIO option SLAM


- 🌱 J'apprends actuellement : **Java, Python**
- ⚡ Fun fact : **Toujours à la recherche de nouveautés**


### Compétences

<a href="https://developer.mozilla.org/fr/docs/Glossary/HTML5" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/732/732212.png" alt="HTML5" width="50" height="50"></a>
<a href="https://developer.mozilla.org/fr/docs/Web/CSS" target="_blank"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/css3-colored.svg" alt="CSS3" width="50" height="50"></a>
<a href="https://developer.mozilla.org/fr/docs/Web/JavaScript" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/1200px-Unofficial_JavaScript_logo_2.svg.png" alt="JavaScript" width="50" height="50"></a>
<a href="https://www.php.net/" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968332.png" alt="PHP" width="50" height="50"></a>

### Stats

<img src="https://github-readme-stats.vercel.app/api?username=Hugo-388&show_icons=true&theme=github_dark" alt="Hugo-388 Github Stats">


<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Hugo-388&langs_count=10&theme=github_dark&hide_border=true&locale=en&custom_title=Top%20%Langage" alt="Top Languages" >

name: generate animation

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the master branch
  push:
    branches:
    - master
    
  

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          hugo-388: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
          
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

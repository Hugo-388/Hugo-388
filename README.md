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

name: 📅 Isometric commit calendar
category: github
description: |
  This plugin displays an isometric view of a user commit calendar along with a few additional statistics like current streak and average number of commit per day.
examples:
  +full year calendar: https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.isocalendar.fullyear.svg
  half year calendar: https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.isocalendar.svg
index: 0
supports:
  - user
scopes:
  - public_access
inputs:

  plugin_isocalendar:
    description: |
      Enable isocalendar plugin
    type: boolean
    default: no

  plugin_isocalendar_duration:
    description: |
      Time range

      - `half-year`: 180 days
      - `full-year`: 1 year
    type: string
    default: half-year
    values:
      - half-year
      - full-year

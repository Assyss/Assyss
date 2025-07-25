<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=0000000&height=120&section=header"/>

[![Typing SVG](https://readme-typing-svg.herokuapp.com/?color=E8D173&size=35&center=true&vCenter=true&width=1000&lines=Hello,+my+name+is+Bruno+Assis;I'm+21+years+old;I'm+from+Brazil;Be+welcome!+:%29)](https://git.io/typing-svg)

<p align="center">
<img src="https://github.com/Assyss/Gif/blob/main/lich.gif" borderradius="50%"/p>
</p>



<div align="center"></div>

<div align="center">  
  <img width="49%" height="195px" src="https://github-readme-stats.vercel.app/api?username=Assyss&show_icons=true&count_private=true&hide_border=true&title_color=E8D173&icon_color=E8D173&text_color=c9d1d9&bg_color=000000" alt="Bruno Assis github stats" /> 
  <img width="41%" height="195px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Assyss&layout=compact&hide_border=true&title_color=E8D173&text_color=c9d1d9&bg_color=000000" />
</div>

<a href="[https://tenor.com/pt-BR/search/hora-de-la-aventura-gifs](https://media1.tenor.com/m/pPdzJD7xxPEAAAAd/malo-hora-de-la-aventura.gif)"></a>

#

<div align="left">
<a href="https://www.linkedin.com/in/bruno-de-assis-7b1316237/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" style="border-radius: 30px" target="_blank"></a> 
<a href="https://www.instagram.com/azyzss/"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"  style="border-radius: 30px" target="_blank">
</div>

 ### Main skills:
![Python](https://img.shields.io/badge/-Python-blue?style=for-the-badge&logo=Python&labelColor=white&textColor=white)&nbsp;
![Java](https://img.shields.io/badge/Java-red?style=for-the-badge&logo=openjdk&logoColor=blue&labelColor=white)&nbsp;
![Node.js](https://img.shields.io/badge/-Node.js-239120?style=for-the-badge&logo=Node.js&labelColor=white)&nbsp;
![JavaScript](https://img.shields.io/badge/-JavaScript-yellow?style=for-the-badge&logo=javascript&labelColor=white)&nbsp;
![HTML5](https://img.shields.io/badge/HTML5-orange?style=for-the-badge&logo=html5&logoColor=orange&labelColor=white)&nbsp;
![CSS3](https://img.shields.io/badge/CSS3-blue?style=for-the-badge&logo=css3&logoColor=blue&labelColor=white)&nbsp;


### Studying in this moment:
![C](https://img.shields.io/badge/C-A4B4C7?style=for-the-badge&logo=c&logoColor=A4B4C7&labelColor=white)&nbsp;
![C++](https://img.shields.io/badge/C%2B%2B-084A86?style=for-the-badge&logo=c%2B%2B&logoColor=084A86&labelColor=white)&nbsp;
![C#](https://img.shields.io/badge/C%23-purple?style=for-the-badge&logo=c-sharp&logoColor=purpl&labelColor=purple)&nbsp;
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)&nbsp;

#

name: Generate Pac-Man Game

on:
  schedule: # Run automatically every 24 hours
    - cron: "0 */24 * * *"
  workflow_dispatch: # Allows manual triggering
  push: # Runs on every push to the main branch
    branches:
      - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: ${{ github.repository_owner }}

      # Push the generated SVG to the output branch
      - name: Push pacman-contribution-graph.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Assyss/Assyss/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Assyss/Assyss/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/Assyss/Assyss/output/pacman-contribution-graph.svg">
</picture>

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=000000&height=120&section=footer"/>

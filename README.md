<h1 align="center">Hi, I'm Thirba 👋</h1>
<p align="center">
  <b>Full-stack developer • Reverse engineering • Windows utilities</b>
</p>
<p align="center">
  <img src="yourphoto.png" width="180" style="border-radius:50%" />
</p>
### When I code, I rely on

![Python](https://img.shields.io/badge/Python-000?style=for-the-badge&logo=python)
![C++](https://img.shields.io/badge/C++-000?style=for-the-badge&logo=cplusplus)
![Windows](https://img.shields.io/badge/Windows-000?style=for-the-badge&logo=windows)
![Reverse Engineering](https://img.shields.io/badge/Reverse_Engineering-000?style=for-the-badge)
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=thirba&show_icons=true&theme=dark&hide_border=true" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=thirba&theme=dark&hide_border=true" />
</p>
name: Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: thirba
          outputs: |
            dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

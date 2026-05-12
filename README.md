<div align="center">

[![Typing SVG](https://readme-typing-svg.herokuapp.com?size=28&duration=3000&center=true&vCenter=true&width=900&lines=Dania+Qistina+Binti+Mazni;Information+Technology+Undergraduate;Future+Technology+Leader;Software+Developer+%7C+UI%2FUX+Designer;Building+Technology+With+Purpose)](https://git.io/typing-svg)

</div>
![GitHub Streak](https://streak-stats.demolab.com/?user=literallymia31)
name: Generate Snake

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
          github_user_name: literallymia31
          outputs: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

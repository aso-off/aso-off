name: Waka Readme

on:
  schedule:
    # Runs at 12am EST
    - cron: '30 18 * * *'
  workflow_dispatch:
jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: aso-off/aso-off@master
        with:
          wakatime: ${{ secrets.wakatime}}
          githubN: ${{ secrets.github }}

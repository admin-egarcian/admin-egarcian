## Hola a todos 👋

- 🔭 **Ingeniero en Redes inteligentes y Ciberseguridad**
+ Aprendiendo GitHub


### Metodos de contacto
+ Telefono
+ Correo

![website](https://img.shields.io/website?url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Fcredentials%2Fcertifications%2Fgithub-foundations%2F%3Fpractice-assessment-type%3Dcertification
)

name: Update README
on:
  schedule:
    - cron: "* */12 * * *"
  workflow_dispatch:
jobs:
  build:
    name: Update this repo's README with recent activity
    runs-on: ubuntu-latest
    permissions:
      contents: write

    steps:
      - uses: actions/checkout@v4
      - uses: admin-egarcian/github-activity-readme@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          COMMIT_MSG: "Specify a custom commit message"
          MAX_LINES: 10
          COMMIT_NAME: GitHub Activity Readme
          COMMIT_EMAIL: github-actions[bot]@users.noreply.github.com
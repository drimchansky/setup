```bash
EXTENSIONS=(
    vscode-colorize
    mikestead.dotenv
    mrcrowl.easy-less
    EditorConfig.EditorConfig
    dbaeumer.vscode-eslint
    mhutchie.git-graph
    eamodio.gitlens
    vincaslt.highlight-matching-tag
    bierner.lit-html
    yzhang.markdown-all-in-one
    sdras.night-owl
    christian-kohler.npm-intellisense
    eseom.nunjucks-template
    christian-kohler.path-intellisense
    csstools.postcss
    esbenp.prettier-vscode
    alefragnani.project-manager
    stylelint.vscode-stylelint
    emmanuelbeziat.vscode-great-icons
    styled-components.vscode-styled-components
    ms-azuretools.vscode-docker
)
for EXTENSION in ${EXTENSIONS[@]}; do
  code --install-extension $EXTENSION
done
```
Copy-paste following to terminal:

```
EXTENSIONS=(
  formulahendry.auto-rename-tag
  bungcip.better-toml
  coenraads.bracket-pair-colorizer
  naumovs.color-highlight
  ms-azuretools.vscode-docker
  mikestead.dotenv
  editorconfig.editorconfig
  dbaeumer.vscode-eslint
  mhutchie.git-graph
  vincaslt.highlight-matching-tag
  wix.vscode-import-cost
  compulim.indent4to2
  kshetline.ligatures-limited
  bierner.lit-html
  yzhang.markdown-all-in-one
  pkief.material-icon-theme
  christian-kohler.npm-intellisense
  zhuangtongfa.material-theme
  christian-kohler.path-intellisense
  mhmadhamster.postcss-language
  stylelint.vscode-stylelint
  esbenp.prettier-vscode
  visualstudioexptteam.vscodeintellicode
  jpoissonnier.vscode-styled-components
)
for EXTENSION in ${EXTENSIONS[@]}; do
  code --install-extension $EXTENSION
done
```
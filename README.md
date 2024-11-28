# Audits

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/iroco-co/audits-frago/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/iroco-co/audits-frago/tree/main)

Audits reports for 
- Accessibility (RGAA)
- Performance (lighthouse)
- Eco-conception (RGESN)
- Green-IT (73 best practices)
- Sobriété éditoriale, 
- Opquast, 
- RSE (Cigref) 

## Local development

```shell
hugo mod get github.com/lowdit/frago
```
Run as a local server

```shell
# Serve locally to http://localhost:1313/audits/
hugo serve
```


## Build for production

```shell
## Build for production
hugo --gc --minify --buildFuture --baseURL https://audits.iroco.co
```

- `--gc` : enable to run some cleanup tasks (remove unused cache files) after the build
- `--minify` : minify any supported output format (HTML, XML etc.)
- `--buildFuture` : include content with publishdate in the future

```shell
# Build for local and preview with vite
hugo --gc --minify --buildFuture --baseURL http://localhost:4173/
npx vite preview --outDir public
```

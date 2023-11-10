# Mise en place de Frago pour Iroco

- [X] Créer un dépôt GIT
  - License? MIT? CC ?
- [ ] Bootstrapper Frago 
  - [X] Theme Frago avec git submodule
  - [X] .gitignore
- [ ] Mettre en place la CI sur CircleCI
- [ ] Déployer avec Ansible
  - [ ] Créer un role clé en main pour installer Frago avec ansible
    - [ ] Créer dépôt `??frago??` dans l’organisation https://github.com/lowdit/
- [ ] Contribuer à Frago
  - Démarrage d’un dépôt Frago
    - [ ] Template GitHub?
      - Pros : facilite le démarrage
      - Cons : on doit le maintenir à jour
        - Ça pourrait se tester automatiquement  
  - Documentation Frago
    - [ ] Hébergement Ansible/Nginx
  - https://lowdit.github.io/frago/docs/demarrer/installer-hugo/#h%C3%A9berger
- [ ] 

## Créer un dépôt Git

Créer dépôt dans github : 

```shell
git init
```

```shell
git remote add origin git@github.com:iroco-co/audits-frago.git
git config pull.rebase true
git branch --set-upstream-to=origin/main main
git pull
git push --set-upstream origin main
```


## Bootstrap Frago

[Installer Hugo](https://lowdit.github.io/frago/docs/demarrer/installer-hugo/).

J’ai choisi d’installer le thème Frago à l’aide des submodules de Git.

```shell
git submodule add -f https://github.com/lowdit/frago.git/ themes/frago && git submodule update --init --recursive && hugo --gc --minify --buildFuture --templateMetrics
```

Tester le site

```shell
hugo serve
```
Ignorer les fichiers générés.

```gitignore
public
.hugo_build.lock
```

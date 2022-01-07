
```Bash
$git init
$git commit -am "Commit initiale"
$git branch develop
$git branch Docker-Compose
ou 
$git switch -c <nouvelle-branch>
$ etc
$git log --online --decorate

# Branches

$git switch develop
$git merge Docker-Compose
$git branch -d <brance-a-supprimer>
$git branch -v # Voir le dernier commit de chaque branche
$git branch --merged # Pour voir quelles branches ont déjà été fusionnées dans votre branche courante
git branch --no-merged #qui contiennent des travaux qui n’ont pas encore été fusionnés
$git branch --move mauvais-nom-de-branche nom-de-branche-corrigé
$git push --set-upstream origin nom-de-branche-corrigé
$git push origin --delete mauvais-nom-de-branche

# Remiser votre travail
$git stash push
$git stash pop


$git log --online --decorate <branche>
$git log --online --decorate all

# Utiliser les Tag 
git tag -a v0.1.0-alpha -m "Message du tag"
git tag -a v0.1.1-beta <idCommit> # Tagger un commit existant
git tag -l
```
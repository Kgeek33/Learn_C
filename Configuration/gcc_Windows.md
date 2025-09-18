# Installer `gcc` sur Windows

`gcc` est le compilateur idéal pour coder en C. De plus, les autres systèmes d'exploitations comme Linux ou encore Mac utilisent ce compilateur (c'est la norme)

## Comment installer ?

1. Ouvre le Terminal (de préférence `cmd`)
2. Écris la commande suivante (_pour installer les composants_)
```
winget install --id "MSYS2.MSYS2" --exact --source winget --accept-source-agreements --disable-interactivity --version "20250830" --silent
```
3. Quand l'installation est terminée, cherche et ouvre l'appli suivante : `MSYS2 MSYS`  (_ou toute appli commençant_ `MSYS2`)
4. Écris la commande suivante (_pour installer les compilateurs_)
```
pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
```
5. Ça demandera : `Enter a selection` => Appuie sur la touche `Entrée` et sur la touche `Y`
6. Quand l'installation est terminée, cherche et ouvre l'appli suivante : `Modifier les variables d’environnement système`
7. En bas, clique sur `Variables d'environnement…`
8. Dans la section `Variables système`, double clique sur `Path`
9. Clique sur `Nouveau` et écris ceci :
```
C:\msys64\ucrt64\bin
```
10. Clique sur `OK` 3 fois

## Comment vérifier que `gcc` est bien installé ?

1. Tout d'abord, ferme tous les terminaux que tu as ouvert (_ou plus simple, redémarre ton PC_)
> Sinon, les modifications des variables d'environnement **ne seront pas prises en compte** !
2. Ouvre le Terminal (de préférence `cmd`)
3. Écris les commandes suivantes :
```
gcc --version
g++ --version
gdb --version
```

> Si tu rencontres une erreur (_commande inconnue_), **refais les étapes** (_surtout **les étapes 6 à 10**_)

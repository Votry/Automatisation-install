1- Creer un dossier du nom du programme (videopslam)
2- Crrer le fichier xml du nuget specification (. nuspec) https://learn.microsoft.com/en-us/nuget/create-packages/creating-a-package
3- Tapez warmup chocolatey videopsalm pour creer les fichier chocolateyinstall.ps1 et chocolateyuninstall.ps1 qui sont dans le dossier tools
4- Modifier le nom du  package, lien , specification dans le fichier xml
5-Modifier le fichier install.PS1 et uninstall PS1
Pour le fichier .msi, pour activer le mode silencieux, on met /quiet comme argument
Pour le fichier.exe, pour activer le mode silencieuw, on met /VERYSILENT
6- Creer le nuget package avec la commande nuget pack videopsalm.nuspec (normalement, il genere un fichier.nupckg)
7-Pour tester l'installation en local choco install videopsalm --soure: C: \..

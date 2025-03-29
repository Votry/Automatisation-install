1- Creer un dossier du nom du programme (videopslam)
2- Crrer le fichier xml du nuget specification (. nuspec) https://learn.microsoft.com/en-us/nuget/create-packages/creating-a-package
3- Tapez warmup chocolatey videopsalm pour creer les fichier chocolateyinstall.ps1 et chocolateyuninstall.ps1 qui sont dans le dossier tools
4- Modifier le nom du  package, lien , specification dans le fichier xml
5-Modifier le fichier install.PS1 et uninstall PS1
Pour le fichier .msi, pour activer le mode silencieux, on met /quiet comme argument
Pour le fichier.exe, pour activer le mode silencieuw, on met /VERYSILENT
6- Creer le nuget package avec la commande nuget pack videopsalm.nuspec (normalement, il genere un fichier.nupckg)
7-Pour tester l'installation en local choco install videopsalm --soure: C: \..
8 - Mettre en ligne le dossier, on se connecte:

git remote add origin https://github.com/Votry/Automatisation-install

Puis on push dans le fichier distant 

git push -u origin master

%Pour pusher le package sur chocolatey.org
1 creer un compte

puis prendre l'API key depuis le compte, se connecter en Admin

choco apikey -k cd00dc57-1d7b-4fd8-8f0a-40c012d4e53a -source https:/push.chocolatey.org/

choco push <pathto package>.nupkg --source https://push.chocolatey.org/
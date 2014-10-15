![Keyboard](background.jpg)

Oh oui, en voilà une belle question.

Il n'est pas toujours évident d'avoir un Linux, Unix, BSD ou autre avec un petit shell bien sympa sous la main. Et parfois coder sous Windows est une nécessité voire un désir. (Ouais, je ne vous parlerai pas ici de changer de boulot si Windows vous est imposé(e) ni de vous expliquer votre déficience mentale d'apprécier cet OS, ce n'est pas le sujet).

Étant un homme de challenge, j'aime me mettre dans des contextes limités et voir comment je me débrouille pour sortir d'une situation pénible à une situation acceptable voire agréable. Je me suis alors lancé pour vous dans cette aventure.

Oh mais pourquoi j'ai dû faire ça à la base ?

Après avoir créé [mon propre système de synchronisation de machines sous Mac OS X](https://github.com/kud/my) (plus souvent communément appelé dotfiles mais faisant un peu plus), j'ai voulu faire de même sous Windows au cas où mon système crasherait et où je devrais tout réinstaller. On n'est jamais à l'abri.

Pour cela, plusieurs outils vont vous être nécessaires. Un chef sans bons outils, c'est drôlement handicapant. (Déjà que l'OS en question n'aide pas).


## Chocolatey : la base

[Chocolatey](http://chocolatey.org/). Ouais, chocolatey, ce petit script vous permettra de télécharger tout et n'importe quoi en cli (ligne de commandes). Pour ceux qui ont l'habitude de mac ou linux, c'est le brew / apt-get de Windows.

Comment l'installer ?

Lancez `cmd.exe` en mode administrateur (touche windows puis "cmd" puis shift+ctrl+enter) et exécutez ce code :

```bash
$ @powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```

Ou `PowerShell` en mode administrateur (touche windows puis "powershell" puis shift+ctrl+enter) et éxecutez :

```bash
$ iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))
```

Une fois installé, vous pourrez installer n'importe quel logiciel listé sur [leur site](http://chocolatey.org/packages).

Passons à la suite.

## Logiciels de développement

Yes, on a donc Chocolatey qui va nous simplifier grandement l'installation de logiciels. Passons maintenant aux outils pour bien développer.

### Git

Lorsque tu joues à un jeu vidéo, tu sauvegardes régulièrement ton avancement non ? Bah là, c'est pareil mais pour le code.

```bash
$ choco install git.install
```

- [site officiel](http://git-scm.com/)
- [lien du package](https://chocolatey.org/packages/git.install)

### Node.js

Faire du JavaScript côté serveur ou en shell, le pied. Surtout pour faire des scripts Windows, plutôt que de passer par Batch.

```bash
$ choco install nodejs.install
```

- [site officiel](http://nodejs.org/)
- [lien du package](https://chocolatey.org/packages/nodejs.install)

### Éditeur de texte

Sublime Text, l'éditeur préféré des Franç... je m'égare. Bref, un bon éditeur.

```bash
$ choco install sublimetext3
```

- [site officiel](http://www.sublimetext.com/)
- [lien du package](https://chocolatey.org/packages/sublimetext3)

Vous pouvez aussi installer [Atom](https://atom.io/) si vous préférez.

### Un meilleur shell

Clink va vous permettre quelques fonctionnalités intéressantes que le shell de Windows n'a pas de base, comme taper `<tab>` pour l'autocomplétion par exemple.

```bash
$ choco install clink.install
```

- [site officiel](http://mridgers.github.io/clink/)
- [lien du package](https://chocolatey.org/packages/clink.install)

### Compresser / décompresser comme vous le voulez

7zip, le logiciel de référence pour ce genre de pratique.

```bash
$ choco install 7zip.install
```

- [site officiel](http://www.7-zip.org/)
- [lien du package](https://chocolatey.org/packages/7zip.install)

### Gérer les pdf

Sumatra pour les lire. PDFCreator pour faire une imprimante virtuelle sortant des PDFs.

#### Sumatra

- [site officiel](http://blog.kowalczyk.info/software/sumatrapdf/free-pdf-reader.html)
- [lien du package](https://chocolatey.org/packages/sumatrapdf.install)

```bash
$ choco install sumatrapdf.install
```

#### PDFCreator

- [site officiel](http://www.pdfforge.org/pdfcreator)
- [lien du package](https://chocolatey.org/packages/pdfcreator)

```bash
$ choco install pdfcreator
```

### Spaaaaaaaces

Parce qu'avoir plusieurs bureaux / espaces, c'est plus pratique pour gérer ses fenêtres, je vous propose VirtuaWin. Cela vous permettra de garder en plein écran vos logiciels et de zapper d'un logiciel à un autre sans passer par alt+tab mais en allant d'un bureau à un autre.

```bash
$ choco install virtuawin
```

- [site officiel](http://virtuawin.sourceforge.net/)
- [lien du package](https://chocolatey.org/packages/virtuawin)

### Launchy, le Alfred-like sous Windows

Je sais pas vous mais moi, les raccourcis qui me gâchent mon beau wallpaper choisi avec goût, ça m'énerve. Et puis le clickodrome, c'est lent et chiant. Du coup, lancer ses logiciels à partir d'un moteur de recherche, c'est quand même vachement bien. Ca permet aussi de faire des recherches de fichier, des calculs, et tout un tas d'autres choses. Voici alors Launchy.

```bash
$ choco install launchy-beta
```

- [site officiel](http://www.launchy.net/)
- [lien du package](https://chocolatey.org/packages/launchy-beta)

### Et enfin, comment ne pas se niquer les yeux toute la journée

#### f.lux

On va commencer par f.lux. Ce petit logiciel permettant de gérer la colorimétrie de votre écran en fonction de l'heure. Typiquement, les écrans rendent un blanc digne d'un soleil à midi. Sauf que le soir, on allume la lumière et celle-ci n'a pas du coup une couleur blanche mais souvent plutôt rouge. f.lux permet alors d'ajuster votre écran afin que la couleur soit identique à la lumière ambiante pour réduire les différences de couleurs et éviter de vous abimer les yeux. En plus, ça permet au cerveau de se préparer à aller se coucher. :D

```bash
$ choco install f.lux
```

- [site officiel](https://justgetflux.com/)
- [lien du package](https://chocolatey.org/packages/f.lux)

#### MacType

Et surtout, MacType. Oh oui MacType. Je pense que seule une personne venant de MacOSX peut comprendre. Dieu sait que le font rendering sous Windows est vraiment pourri et que Steve Jobs depuis le départ de Mac a fait en sorte sur le rendering des fonts sous son OS soit de qualité.

Pour réduire cette différence entre un Windows et un MacOSX, je vous propose MacType qui permet de remplacer le font rendering de Windows et d'apprécier lire à nouveau sur cet OS.

```bash
$ choco install mactype
```

Je vous conseille le profil `XMac.LCD.Default`.

- [site officiel](https://code.google.com/p/mactype/)
- [lien du package](https://chocolatey.org/packages/mactype)

## Vous voilà paré(e) !

On est bon, on a tous les outils nécessaires pour pouvoir coder correctement sur Windows.

Si vous souhaitez en savoir plus et surtout vous tenir à jour d'éventuels logiciels que je pourrais installer, n'hésitez pas à vous rendre sur mon projet [my-unfortunately](https://github.com/kud/my-unfortunately) qui est le _synchroniser_ dont je vous ai parlé tout à l'heure.

Bon code !
# Git-Introduction

![Git Bild](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/640px-Git-logo.svg.png)

### In diesem Dokument könnt ihr den Ablauf der Git Präsentation mitverfolgen bzw wiederholen.

## Schritte zur Aufsetzung:

1. Installiere **Git** auf deinem System [Git Download](https://git-scm.com/downloads)
2. Erstelle ein Private Remote Git Repository auf [Github](https://github.com)
3. **Klicke dabei nicht auf ReadME erstellen und gebe keine Beschreibung!**
4. Erstelle ein neues ***Java Projekt*** in **IntelliJ**
5. Bevor wir den ersten Code ins Projekt schreiben werden das Github Repo initialisieren.
6. Nach der Initialisierung werden wir unser Remote Git Respository mit unserem Lokalem verknüpfen und den Code Demo Code hochladen (push)

---

### Git Ignore File:

Füge dieses File zu deinem Projekt hinzu, falls es das noch nicht gibt:

Filename: ***.gitignore***
```
### IntelliJ IDEA ###
out/
!**/src/main/**/out/
!**/src/test/**/out/

### Eclipse ###
.apt_generated
.classpath
.factorypath
.project
.settings
.springBeans
.sts4-cache
bin/
!**/src/main/**/bin/
!**/src/test/**/bin/

### NetBeans ###
/nbproject/private/
/nbbuild/
/dist/
/nbdist/
/.nb-gradle/

### VS Code ###
.vscode/

### Mac OS ###
.DS_Store
```

### Commands für Aufsetzung:

Öffne ein Terminal in deinem IntelliJ Projekt. Vergewissere dich, dass du ein Powershell Terminal verwendest.

Danach kopiere diese Befehle und führe sie im Terminal einmal aus:

```
 git init .
 git checkout -b main
 git add .
 git commit -m 'init repo'
 git remote add origin <http-remote-url (in deinem repo auf github)>
 git push origin main
```

***Wenn alles geklappt hat, dann kannst du nun auf deinem Remote Repo auf Github überprüfen, ob dein Code hochgeladen wurde.***

---

## Durchführung der Git-Übung:

1. Code commiten und pushen
2. Branches erstellen und verwalten
3. Branches Mergen und Merge Conflicts vermeiden
4. Übungsbeispiel

---

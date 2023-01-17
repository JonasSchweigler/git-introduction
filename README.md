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
---



# Code Snippets 

Beans-Klasse "Person.java":
```java
package at.htlkaindorf.beans;

public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }


    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return String.format("%s - %d", name, age);
    }
}
```

UI-Klasse "Main.java":
```java
package at.htlkaindorf.ui;

import at.htlkaindorf.beans.Person;

public class Main {
    public static void main(String[] args) {
        Person jan = new Person("Jan Fofnjka", 16);
        System.out.println("Name - Age");
        System.out.println(jan);
    }
}
```

## Ablauf des Version-Controls

1.) Neuen Zweig "person-class" erstellen
```git
git checkout -b person-class
```
2.) Den Code in die richtige Datei einfügen 

3.) Die Veränderungen ansehen und hinzufügen:
```git
git status
git add .
```

4.) Einen "Commit" ausführen
```git
git add .
git commit -m "created Person.java"
```

4.) Einen weiteren Branch für die Main-Klasse erstellen
```git
git checkout main
git checkout -b main-class
```

5.) Den Code einfügen


6.) Die Veränderungen ansehen und hinzufügen:
```git
git status
git add .
```

7.) Einen "Commit" ausführen
```git
git add .
git commit -m "created Main.java"
```

8.) Die beiden Branches EXTRA pushen (zur Demonstation)
```git
git push -u origin person-class
git push -u origin main-class
```

9.) Überprüfe ob die beiden Branches in deinem Remote-Repo (Github) existieren


10.) Zusammenführen der Branches (lokal)

```git
git checkout main
git merge person-class
git merge main-class
```


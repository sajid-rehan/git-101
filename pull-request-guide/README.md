# Git Pull Requests

## Anleitung zum Erstellen von Pull Requests

Herzlich willkommen zur Anleitung für Pull Requests! Du kannst gerne diese Anleitung mitverfolgen, indem du sie auf unserem Team-[Playground-Repository](https://github.com/110-Devs/playground) anwendest, das eigens dazu dient, deine Git Fähigkeiten zu verfeinern.

## Inhaltsverzeichnis
- [Git Pull Requests](#git-pull-requests)
  - [Anleitung zum Erstellen von Pull Requests](#anleitung-zum-erstellen-von-pull-requests)
  - [Inhaltsverzeichnis](#inhaltsverzeichnis)
    - [Begriffserklärung](#begriffserklärung)
  - [1. **Fork des Repositories**](#1-fork-des-repositories)
  - [2. **Lokale Kopie klonen**](#2-lokale-kopie-klonen)
  - [3. **Einen neuen Branch erstellen**](#3-einen-neuen-branch-erstellen)
    - [3.1. **Änderungen vornehmen**](#31-änderungen-vornehmen)
    - [3.2. **Push des Branches**](#32-push-des-branches)
  - [4. **Pull Request erstellen**](#4-pull-request-erstellen)
  - [5. **Diskussion und Überprüfung (WIP):**](#5-diskussion-und-überprüfung-wip)
    - [5.1. **Merge des Pull Requests**](#51-merge-des-pull-requests)
  - [6. Origin-Repository aktualisieren](#6-origin-repository-aktualisieren)

### Begriffserklärung

Zu Beginn möchten wir kurz einige Begriffe klären, um sicherzustellen, dass wir alle auf dem gleichen Stand sind. Die Begriffe "upstream", "origin", "remote" und "local" sind grundlegend für das Verständnis von Git.

Hier ist eine Grafik, die diese Konzepte visuell darstellt (Die ausgegrauten Begriffe und Pfeile sind vorerst nicht relevant, werden jedoch im Verlauf des Tutorials alle erklärt):

![Begriffserklärung](assets/img/overview_00_light.png#gh-light-mode-only)
![Begriffserklärung](assets/img/overview_00_dark.png#gh-dark-mode-only)

- **Upstream:** Der "upstream" bezieht sich auf das ursprüngliche Repository, von dem ein Fork erstellt wurde. In einem typischen Workflow mit Forks und Pull Requests ist "upstream" das Hauptrepository, in dem Änderungen zusammengeführt werden sollen. In unserem Beispiel ist dies das [110-Devs/playground](https://github.com/110-Devs/playground)-Repository.

- **Origin:** "Origin" ist das Remote-Repository, von dem ein lokales Repository geklont wurde, bzw. in diesem Fall auch das Repository, das durch das Forken des Upstreams entstanden ist.

- **Remote:** Ein "Remote" bezieht sich auf ein entferntes Repository, das von Git verwaltet wird. Es kann auf einem Server oder einem anderen Speicherort gespeichert sein. Remotes werden verwendet, um mit Repositories außerhalb des lokalen Systems zu interagieren, wie z.B. das Abrufen von Änderungen von einem entfernten Repository oder das Hochladen lokaler Änderungen auf ein entferntes Repository.

- **Local:** "Local" bezieht sich auf das lokale Repository, das auf deinem Rechner gespeichert ist.

## 1. **Fork des Repositories**

Beginne damit, das Repository, an dem du arbeitest, zu forken. Dadurch wird eine Kopie des [Upstream-Repositorys](https://github.com/110-Devs/playground) in deinem GitHub-Konto erstellt. Navigiere dafür zu unserem [Upstream-Repository](https://github.com/110-Devs/playground) und klicke auf "Fork".

![Fork beispeil](assets/img/fork_light.png#gh-light-mode-only)
![Fork beispeil](assets/img/fork_dark.png#gh-dark-mode-only)

Wähle auf dem nachfolgenden Fenster dein GitHub-Konto aus, auf das geforkt werden soll. Die Standardeinstellungen können übernommen werden, klicke dann auf "Create fork".

![Fork erstellen](assets/img/create_fork_dark.png#gh-dark-mode-only)
![Fork erstellen](assets/img/create_fork_light.png#gh-light-mode-only)

Damit wäre der Fork-Vorgang abgeschlossen.

![Übersicht](assets/img/overview_01_light.png#gh-light-mode-only)
![Übersicht](assets/img/overview_01_dark.png#gh-dark-mode-only)

## 2. **Lokale Kopie klonen**

Lass uns nun das Repository von deinem Fork auf deinem lokalen Rechner klonen. Öffne dazu dein Terminal und navigiere zum Ordner, in den das Repository geklont werden soll. Führe dann den folgenden Befehl aus:

```bash
git clone git@github.com:<github_account>/<repo>.git
```

Ersetze dabei `<github_account>` durch deinen GitHub-Benutzernamen und `<repo>` durch den Namen des Repositories, in unserem Fall "playground".

![Übersicht](assets/img/overview_02_light.png#gh-light-mode-only)
![Übersicht](assets/img/overview_02_dark.png#gh-dark-mode-only)

## 3. **Einen neuen Branch erstellen**

Erstelle einen neuen Branch für deine Änderungen:

```bash
git checkout -b mein-feature-branch
```

### 3.1. **Änderungen vornehmen**

Nimm nun die gewünschten Änderungen am Code vor / implementiere das neue Feature und erstelle anschließend Commits.

### 3.2. **Push des Branches**

Sobald alle Änderungen auf dem neu erstellten Branch `mein-feature-branch` vorgenommen wurden, können sie in das Origin-Repository bzw. Fork-Repository gepusht werden.

```bash
git push origin mein-feature-branch
```

![Übersicht](assets/img/overview_03_light.png#gh-light-mode-only)
![Übersicht](assets/img/overview_03_dark.png#gh-dark-mode-only)

Wenn alle Änderungen im Remote-Repository (origin) vorhanden sind, können wir mit dem Erstellen des Pull Requests fortfahren.

## 4. **Pull Request erstellen**

Nachdem du deine Änderungen gepusht hast, solltest du eine Benachrichtigung auf der GitHub-Seite deines Origin-Repositories bezüglich des letzten Push erhalten (siehe nachfolgende Bild).

![Push-Benachrichtigung](assets/img/push_notification_light.png#gh-light-mode-only)
![Push-Benachrichtigung](assets/img/push_notification_dark.png#gh-dark-mode-only)

Du kannst nun den Prozess zum Erstellen eines neuen Pull Requests starten, indem du entweder auf die grüne Schaltfläche "Compare & pull request" **oder** auf die "Contribute"-Schaltfläche klickst und dann "Open pull request" auswählst.

![contribution-beispiel](assets/img/contribution_light.png#gh-light-mode-only)
![contribution-beispiel](assets/img/contribution_dark.png#gh-dark-mode-only)

Unabhängig davon, welche Option du wählst (ob über "Compare & pull request" oder "Open pull request"), wirst du zur Seite weitergeleitet, auf der der Pull Request gestellt werden kann.

Auf dieser Seite musst du sowohl das Upstream- als auch das Origin-Repository sowie die Branches angeben, in dem deine Änderungen gemerged werden sollen, falls der Pull Request akzeptiert wird. Dies mag ein wenig kompliziert klingen, ist es aber nicht. Auf der Seite wird es folgendermaßen dargestellt:

![branch-comparing](assets/img/branch_comparing_light.png#gh-light-mode-only)
![branch-comparing](assets/img/branch_comparing_dark.png#gh-dark-mode-only)

Rechts vom Pfeil steht **"head repository"** und **"compare"**. Das **"head repository"** ist dein Fork-Repository und **"compare"** ist der Branch, der die Änderungen enthält, die im Upstream-Repository gemerged werden sollen – in unserem Fall ist dies der `mein-feature-branch`.

Links vom Pfeil steht **"base repository"** und **"base"**. Das **"base repository"** ist das Upstream-Repository und **"base"** ist der Branch in den deine Änderungen im Falle der Annahme des Pull Requests gemerged werden sollen.

Gib nun eine aussagekräftige Beschreibung für deinen Pull Request im Beschreibungsfeld ein und klicke auf die grüne Schaltfläche "Create pull request", um den Pull Request zu stellen.

![Übersicht](assets/img/overview_04_light.png#gh-light-mode-only)
![Übersicht](assets/img/overview_04_dark.png#gh-dark-mode-only)

## 5. **Diskussion und Überprüfung (WIP):**

- Andere Teammitglieder können deine vorgeschlagenen Änderungen überprüfen und Feedback geben.

### 5.1. **Merge des Pull Requests**

- Wenn alles überprüft wurde und das Feedback berücksichtigt wurde, kann der Pull Request in den Hauptbranch bzw. den Branch, der beim Stellen des Pull Requests angegeben wurde, fusioniert werden.

Da in unserem Team nur eine begrenzte Anzahl von Entwicklern Pull Requests überprüfen, werden ich hier nicht weiter auf reviewen der Pull requests eingehen. Wenn du jedoch daran interessiert bist, kannst du gerne:

- Videos zum Reviewen eines Pull Requests anschauen, um zu sehen, wie dies idealerweise durchgeführt wird.
- Ebenfalls gibt es Online-Dokumentationen dazu, die ebenfalls hilfreich sein können.

Für den Zweck der Übung kannst du, nachdem du deinen Pull Request gestellt hast,
1. zum [Upstream-Repository](https://github.com/110-Devs/playground) navigieren. 
2. Klicke oben in der Liste auf [Pull requests](https://github.com/110-Devs/playground/pulls),
3. wähle deinen Pull Request aus der Liste aus und

![Merge pull request](assets/img/merge_pr_light.png#gh-light-mode-only)
![Merge pull request](assets/img/merge_pr_dark.png#gh-dark-mode-only)

4. klicke dann auf die grüne Schaltfläche "Merge pull request".

Somit wäre der Pull Request erfolgreich gemerged.

## 6. Origin-Repository aktualisieren

Während du gerade an einem Feature arbeiten könntest, arbeiten auch andere Teammitglieder parallel an anderen Features. Diese Features werden dann in den `main`-Branch des [Upstream-Repositorys](https://github.com/110-Devs/playground) gemerged. Diese Änderungen im Upstream-`main`-Branch sind natürlich nicht automatisch mit deinem lokalen `main`-Branch synchronisiert.

Um diese neuen Änderungen vom Upstream-Repository zu holen, musst du zuerst sicherstellen, dass Git das [Upstream-Repository](https://github.com/110-Devs/playground) kennt. Navigiere dazu über das Terminal oder die CMD zu deinem lokalen Repository und gib den folgenden Befehl ein:

```bash
git remote add upstream git@github.com:110-Devs/playground.git
```

Wenn du nun:

```bash
git remote -v
```

eingibst, solltest du sowohl dein Origin-Repository als auch das Upstream-Repository sehen.

Dann kannst du mit:

```bash
git fetch upstream
```

alle neuen Änderungen im `main`-Branch und allen anderen Branches vom Upstream-Repository holen.

![Übersicht](assets/img/overview_05_light.png#gh-light-mode-only)
![Übersicht](assets/img/overview_05_dark.png#gh-dark-mode-only)

Dein lokaler `main`-Branch ist jedoch immer noch nicht auf dem neuesten Stand. Überprüfe dies mit `git log`, um festzustellen, dass der letzte Commit deines lokalen `main`-Branches immer noch nicht mit dem Upstream-`main`-Branch übereinstimmt.

Um die beiden Branches zu synchronisieren, wechsle zuerst zu deinem `main`-Branch mit

```bash
git checkout main
```

und führe dann den folgenden Befehl aus:

```bash
git reset --hard upstream/main
```

Nun sollten dein lokales Repository und das Upstream-Repository synchron sein, aber dein Origin-Repository noch nicht. Um dies zu erreichen, musst du nur noch die neuen Änderungen in dein Origin-Repository pushen.

```bash
git push origin main
```

Dies mag am Anfang etwas verwirrend sein, den Überblick darüber zu behalten, wo was gepullt wird, synchronisiert wird oder gepusht wird. Deshalb kannst du, wann immer du den Upstream-`main`-Branch sowohl lokal als auch mit dem Origin synchronisieren möchtest, einfach die folgenden Befehle in der Reihenfolge im Terminal eingeben (vorausgesetzt du hast den Upstream bereits als Remote eingerichtet!):

1. `git fetch upstream`
2. `git checkout main`
3. `git reset --hard upstream/main`
4. `git push origin main`

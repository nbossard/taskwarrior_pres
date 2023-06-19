# Taskwarrior

Pourquoi on accroche?

![[taskwarrior_logo.png]]

Nicolas BOSSARD. 
20 Juin 2023. <br/>
Software Crafters Rennes

note: pres écrite avec : 
- Obsidian 
- plugin "advanced slides"  (reveal.js)
	- <https://github.com/MSzturc/obsidian-advanced-slides>
	- <https://mszturc.github.io/obsidian-advanced-slides/>
 - Press the »S« key on your keyboard to open the notes window

---

## Qui suis-je?

<split even gap="1">
<split even gap="1">
![[orange_logo.svg| 60]]
![[Mahali.jpg]]
</split>

Développeur chez Orange Innovation Rennes.

Intérêt particulier pour les outils :

<split even>
![[copilot.jpg]]
![[neovim.jpg]] 
![[plantuml.jpg]]
![[anki.jpg]]
</split>
</split>

note: 
- Startup interne Mahali
- Merci à **Pascal LE MERRER** invit
- développeur fullstack / surveillance prod ==> beaucoup de choses à faire et penser
- 

---

<grid drag="100 55" drop="top" flow="col" align="stretch">
## Les todo list...

De multiples essais. 

En plus de nos taiga/JIRA/gitlab...
Parfois les logiciels ont disparu / devenus payants / la liste devenait immense... / fastidieux

</grid>

<grid drag="100 45" drop="bottom" flow="row" align="stretch">
![[astrid.jpeg]] 
![[yahoo_rip.png]]
</grid>
---

Et puis... taskwarrior, bizarrement le temps passe 

![[task_3_ans.png]]

et je l'utilise toujours tous les jours, de plus en plus!!!

**Qu'est ce qui a fait la différence?**

Note: 
- dans le terminal ligne de commande
- grand AMOUR : 1600 tâches créées

---

## La beauté? l'IHM aux petits oignons? l'ergonomie?  👎
![[empty_task_list.png]]

<!-- terminal based, sic -->

---

## Le prix  👍

Free open source, activement maintenu.
![[commits_graph.png]]

Note: 
- tourne en local
- pas d'abonnement
- https://github.com/GothenburgBitFactory/taskwarrior
- V1.0.0 2008

---

## simplcité 👍

![[task_basic.png]]

Note:  
- utilisable immédiatement
- détailler la copie écran

---

## mais en a sous le capot 👍

- couleur
- thèmes
- context (work / pro)
- projects
- priority (High / low /...)
- tags (PERSO/...)
- dépendances
- annotations
- ...

Note: un peu comme vim

---

## peut s'échapper du terminal 👍

système de synchronisation intégré

`task sync`

- inthe.am ===> **task server** + disponible sur le web 
- foreground ==> client  android avec **task sync** 
- ![[foreground_icon.png| 50x]]

--

![[inthe.am_screenshots.png]]

--

![[foreground_screenshot.png]]

---

## La vitesse 👍

1600 tâches créées

- `task add` ===> instantané
- `task next` ===> instantané
- `task burndown.monthly` ==>  1-2 secs

--

t stats

```text
Category                   Data
Pending                    35
Waiting                    29
Recurring                  0
Completed                  1171
Deleted                    349
Total                      1584 <============== TOTAL
Annotations                695
Unique tags                38
Projects                   18
Blocked tasks              6
Blocking tasks             9
Data size                  5.9 MiB
Undo transactions          10642
Sync backlog transactions  430
Tasks tagged               6.94%
Oldest task                2021-04-30
Newest task                2023-06-17
Task used for              2.1y
Task added every           11h
Task completed every       15h
Task deleted every         2d
Average time pending       12d
Average desc length        43 characters
```

---

## Structure de données simple et efficace 👍

4 fichiers textes
  - pending.data ==> tâches à faire (taille réduite)
  - completed.data ==> tâches finies (peut grossir)
  - backlog.data ==> tâches à synchroniser
  - undo.data ==> undo list

note: 
debuggable si besoin
dans dossier ".task"
pas de bd, simple, super efficace

---

## les super rapports 💤

![[graph_report.png]]

note: 
- task reports
- plutôt joli pour du terminal
- personnellement inutilisé, on utilise toujours le même customisé
- taper `task report`pour avoir une liste des rapports possible
--

## les super rapports 💤

![[report_calendar.png]]

---

## ...j'utilise toujours le même rapport

![[report_next.png]]

--

![[report_next.png| 100%]]

Note: 
`task color legend`

- détailler le contenu de la liste
- parler de l'ordonnancement

---

## Fonctions clé 👍

![[task_detail.png]]

note: parler de
- calcul de l'urgence
- système de date  "due date"
- système de "wait"
- annotations
- virtual tags

--

- système de date  "due date"
- système de wait
- annotations

---

## Logiciels de l'écosystème👍


--

### Ecosystème :  Bugwarrior 💤

<https://github.com/ralphbean/bugwarrior>

note: 
installation : 
`pip install bugwarrior`

configuration: see file ~/.config/bugwarrior/bugwarriorrc

usage : 
`bugwarrior-pull --dry-run`

--

### Ecosystème : timewarrior 💤
![[timewarrior.png]]

--

### Ecosystème TUI 💤

![[tui.png|650]]

--

### Nombreux outils


![[810_tools.png]]

---

## Mais surtout les vôtres 👍

- hook API ==> exécution à la volée
- export ==> nouvelles présentations

--

### taskwarrior hook add annotation 🪡

<https://github.com/nbossard/taskwarrior-hook-addannotation>


```
task add "Fixing MR222"

🪄HookAddAnnotation: Found prefix "MR"
🪄HookAddAnnotation: ✅ Added annotation "https://taiga.tech.orange/project/thommil-mahali-poc/merge-request/222"

Created task 73.
```

--

### taskplantdep 🪡

<https://github.com/nbossard/taskplantdep>

![[taskplantdep.png]]

---

## Bref

- super outil : 
	- rapide 
	- stable 
	- addictif 
	- riche en fonctionnalités 
	- extensible

-  `sudo apt install taskwarrior` / <br/> `brew install taskwarrior`

*...des questions ?*
En quel language écrit

---

## contact

nicolas.bossard@machboboss.ovh

![[mastodon.jpg| 60x]]
@nbossard@mastodon.iriseden.eu

TODO : lien repo

---

## Historique de la présentation

- 2023-06-07 début écriture pres
- 2023-06-19 présentation à [[Vincent MAHE]]
- 2023-06-20 présentation à meetup software craftmen Rennes

# Aube

Programme du matin pour atteindre **100 pompes et 300 crunchs d'affilée**.
Six séances par semaine (du lundi au samedi), environ 30 minutes souplesse comprise, repos le dimanche avec une séance d'étirements doux facultative.

L'appli tient en quelques fichiers statiques. Elle n'utilise aucun serveur, aucun compte,
aucune API et aucune intelligence artificielle : elle fonctionne hors ligne, aussi longtemps
qu'un navigateur saura ouvrir une page web.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | Toute l'appli : programme, interface, polices. |
| `manifest.webmanifest` | Permet l'installation sur l'écran d'accueil. |
| `sw.js` | Fait fonctionner l'appli sans connexion. |
| `icon-192.png`, `icon-512.png`, `icon-maskable.png` | Icônes. |

Garde une copie de ce dossier (ou du fichier zip) dans un endroit sûr : Google Drive, clé USB, mail à toi-même.

## Mettre l'appli en ligne (une seule fois, gratuit)

Pour s'installer sur Android, l'appli doit être servie en `https`. GitHub Pages le fait gratuitement et sans limite de durée.

1. Crée un compte sur **github.com** (gratuit).
2. En haut à droite, **+** puis **New repository**. Nom : `aube`. Coche **Public**. Clique **Create repository**.
3. Sur la page du dépôt, clique **uploading an existing file**. Glisse-dépose les fichiers du dossier (`index.html`, `manifest.webmanifest`, `sw.js` et les trois icônes). Clique **Commit changes**.
4. Va dans **Settings** puis **Pages**. Sous *Branch*, choisis `main` et `/ (root)`, puis **Save**.
5. Après une à deux minutes, l'adresse s'affiche en haut de la page : `https://TON-PSEUDO.github.io/aube/`.

Le dépôt public ne contient que le code de l'appli. Tes séances et tes records ne quittent jamais ton téléphone.

**Autres hébergeurs possibles** (même principe : déposer le dossier) : Netlify (app.netlify.com/drop, crée ensuite un compte dans l'heure pour garder le site), Cloudflare Pages, ou n'importe quel hébergement web en https.

## Installer sur Android

1. Ouvre l'adresse dans **Chrome**.
2. Appuie sur le bouton **Installer** dans l'appli, ou sur le menu **⋮** puis **Installer l'application** (parfois « Ajouter à l'écran d'accueil »).
3. Aube apparaît avec les autres applis. Elle s'ouvre en plein écran et marche sans réseau.

## Rappel du matin

Une appli web ne peut pas sonner seule à heure fixe sans serveur. Deux solutions fiables :
- dans **Réglages > Rappel du matin**, le bouton crée un événement Google Agenda récurrent du lundi au samedi ;
- ou un réveil Android répété du lundi au samedi, nommé « Aube ».

## Sauvegarder et changer de téléphone

Les données sont stockées dans le navigateur du téléphone. Elles ne sont effacées que si tu désinstalles l'appli ou vides les données de Chrome pour ce site.

- **Réglages > Sauvegarde > Envoyer…** : envoie un fichier `.json` vers Google Drive, Gmail, etc. Fais-le toutes les deux ou trois semaines (l'appli te le rappelle).
- Sur un nouveau téléphone : installe l'appli depuis la même adresse, puis **Réglages > Sauvegarde > Restaurer un fichier**.

## Comment le programme fonctionne

- **Test de départ** : ton maximum de pompes, 3 minutes de pause, ton maximum de crunchs.
- **Semaine type** : grosses séances de pompes lundi (classique), mercredi (pyramide), vendredi (densité), toujours séparées de 48 h de récupération ; grosses séances de crunchs mardi (classique), jeudi (endurance), samedi (densité). Les abdos travaillent aussi les jours de pompes (3 séries modérées). Les jours d'abdos, 2 petites séries de pompes très faciles entretiennent le geste (désactivables dans les réglages). Chaque séance ajoute un bloc jambes, dos, cardio ou mobilité, un échauffement et des étirements.
- **Cycle de 4 semaines** : construction, progression, surcharge, puis une semaine allégée terminée par un test le samedi.
- **Souplesse** : chaque séance finit par 5 à 9 minutes d'étirements statiques. Trois thèmes reviennent deux fois par semaine (hanches et adducteurs, ischios et mollets, hanches, cuisses et fessiers). Le repère de maintien passe de 30 à 60 secondes au fil des cycles et s'ajuste selon ce que tu tiens vraiment. Le chrono sonne au repère mais ne passe jamais tout seul. Le dimanche, une séance douce facultative d'environ 15 minutes. Un bilan au mètre ruban (doigts-sol, écart des talons, papillon) revient avec chaque test.
- **Ordre des exercices** : debout d'abord, puis à genoux, à quatre pattes, sur le ventre, assis et sur le dos. Chaque exercice d'échauffement et chaque étirement attend ton « Go ».
- **Adaptation** : après chaque séance, tu indiques ton ressenti. Séries réussies : +1 niveau (environ +4 % de capacité). Trop facile : +2. Trop dur ou séries manquées : −1. Douleur : −2. Après plus de 10 jours d'arrêt, le programme s'allège ; après 3 semaines, il propose un nouveau test.
- **Récompenses** : XP à chaque répétition et chaque minute d'étirement, niveaux et titres, série de séances protégée par des jokers, 35 médailles, records, projection de la date d'objectif.

Le détail et les sources sont dans l'appli : **Réglages > La méthode et les sources**.

## Le guide des gestes

L'onglet **Gestes** présente les 43 exercices du programme avec une animation, les muscles travaillés, les points clés, les erreurs fréquentes, une version plus facile et une plus difficile. Pendant la séance, l'animation de l'exercice en cours s'affiche à l'écran, et le lien « Détails » ouvre la fiche complète.

## Modifier l'appli plus tard

Tout le code est dans `index.html`, lisible avec n'importe quel éditeur de texte. Les réglages du programme (formats, pourcentages, cycle) sont regroupés au début du premier bloc `<script>`, dans les constantes `EX`, `FORMATS`, `WEEK` et `PHASES`. Après une modification, dépose le nouveau fichier au même endroit et change le numéro dans `sw.js` (par exemple `aube-1.2.0` → `aube-1.2.1`) : les téléphones installent alors la nouvelle version à l'ouverture suivante.

## Crédits

Polices sous licence SIL Open Font License 1.1 : Big Shoulders Display (Patric King) et Figtree (Erik Kennedy).

Aube ne remplace pas un avis médical. Douleur vive, gêne dans la poitrine ou essoufflement inhabituel : arrête et consulte.

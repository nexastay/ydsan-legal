# Conditions d'utilisation et politique de confidentialité

**Ydsan** — assistant personnel
Version 2.3 — 6 septembre 2026
Contact : contact.ydsan@gmail.com

Ce texte dit ce que Ydsan fait de tes données. Il est écrit pour être vérifié :
chaque phrase décrit un comportement réel du logiciel, pas une intention.

---

## 1. Ce que c'est

Ydsan est un assistant personnel : il répond, pose des rappels et des réveils,
tient un agenda, permet d'écrire à des contacts, fabrique des documents et des
images, et peut ouvrir les applications de ton téléphone.

Il existe sous deux formes — une page web, et une application Android. Les deux
parlent au même compte.

En utilisant Ydsan, tu acceptes ce qui suit. Si un point te gêne, écris à
l'adresse ci-dessus : une objection vaut mieux qu'un abandon silencieux.

---

## 2. Ce qui est gardé, et où

### Ton compte

Ton **courriel**, la date de création, ton palier, et tes réglages.

**Ton mot de passe n'est jamais gardé.** Ce qui est écrit, c'est un sel
aléatoire et une empreinte PBKDF2-SHA256 à 600 000 tours. Personne — pas même
l'administrateur — ne peut le relire ; il ne peut être que *vérifié*.

Ton **jeton d'accès** n'est pas gardé non plus. Il se recalcule de ton courriel
avec une clé qui ne quitte jamais la machine du service. Changer ton mot de
passe ne te fait donc pas perdre ton compte.

### Tes conversations

Elles sont gardées pour que tu les retrouves d'un appareil à l'autre. Tu peux
en **supprimer** n'importe laquelle depuis l'application.

### Ce que tu crées dans l'application

Contacts, messages, réveils, minuteurs, fuseaux suivis, rendez-vous, rappels,
documents et images fabriqués à ta demande, **extensions** et **agents**. Ils
t'appartiennent, et **toi seul** les lis : la base refuse une lecture qui ne
vient pas de ton compte (*Row Level Security*), ce n'est pas une promesse mais
une règle appliquée par le moteur de base de données.

### Les extensions et les agents

Tu peux demander à Ydsan de te **fabriquer une page** — un suivi de dépenses,
un carnet de recettes, une liste — et d'y attacher un **agent** qui se réveille
tout seul pour y ajouter une ligne.

Ce que fait un agent, et ce qu'il ne fait pas :

- il ne connaît **que sa page**. Ni tes contacts, ni tes messages, ni tes
  réveils, ni ton agenda, ni les autres extensions ;
- il **ne va pas sur internet** et ne communique avec personne ;
- il n'écrit **qu'à toi**, dans ta page, et te prévient par une notification ;
- tu peux l'**éteindre** ou le supprimer à tout moment depuis sa page.

Une extension et son agent n'existent **que chez toi**. Aucun autre utilisateur
ne les voit, et personne ne peut lire ce qu'il y a dedans.

### Deux pages qui se lisent

Tu peux **lier** deux de tes extensions pour qu'un agent croise les deux.
C'est la seule exception à la règle « un agent ne connaît que sa page », et
elle est entièrement entre tes mains : le lien se pose **à ta demande**, il va
**dans un seul sens**, et la page liée est en **lecture seule**. Ydsan ne lie
jamais deux pages de lui-même.

### À qui appartient ce qui est fabriqué

Il faut distinguer deux choses, et la distinction est simple.

**Le logiciel reste à Ydsan.** L'application, ses pages, la façon dont une
extension est construite et affichée, le mécanisme des agents, le code qui fait
tout cela : c'est la propriété de l'éditeur d'Ydsan. Tu en as un **droit
d'usage** pendant la durée de ton abonnement — tu ne peux ni le revendre, ni le
copier, ni le redistribuer. Une extension fabriquée pour toi n'est pas un
produit que tu peux commercialiser.

**Ce que tu mets dedans est à toi.** Les lignes que tu saisis, celles que ton
agent ajoute pour toi, les noms que tu donnes, ce que tu écris : ce sont **tes
données**, elles t'appartiennent, et rien de tout cela ne devient la propriété
d'Ydsan. Tu peux les exporter, les corriger, les effacer. Le jour où tu
supprimes ton compte, elles partent avec.

Autrement dit : **le carnet est à Ydsan, ce qui est écrit dedans est à toi.**

### Ce qu'il retient de toi

Ydsan garde une **mémoire longue** : ce que tu lui dis de durable sur toi — ce
qui compte pour toi, tes projets, tes goûts, ta façon de faire. Chaque souvenir
porte **la date où tu l'as dit**, et il s'en sert pour te répondre.

Deux façons dont un souvenir arrive :

- **tu le lui demandes** (« retiens que… »), ou tu le lui apprends en parlant ;
- **il relit tes conversations de la veille**, une fois par jour, et en retient
  ce qui vaudra encore dans six mois. Ces souvenirs-là sont marqués
  « déduit » — il peut se tromper, et tu le vois.

**Tout est visible, et tout se retire.** Dans ⚙ Profil, « Ce qu'il sait de
toi » : chaque souvenir, sa date, et une croix. Un souvenir retiré est
supprimé, pas mis de côté.

Quand tu le contredis, l'ancien souvenir n'est **pas effacé** : il est éteint et
gardé avec sa date. C'est ce qui lui permet de dire « tu me disais l'inverse en
juin ». Tu peux le supprimer aussi.

Rien de cela ne sort de ton compte. La base refuse une lecture qui ne vient pas
de toi, comme pour le reste.

### Ce qu'il te propose sans que tu demandes

Ydsan regarde ton agenda, tes réveils et tes agents, et il peut te **proposer**
quelque chose : « rendez-vous demain à 8 h 30, aucun réveil — je t'en pose
un ? ». C'est du code qui remarque, pas une intelligence qui devine : chaque
suggestion repose sur **une ligne qui existe déjà** dans ton compte, et rien
n'est cherché à l'extérieur.

Les règles, qui sont dans le logiciel et pas seulement dans ce texte :

- **deux par jour au maximum**, et jamais deux fois la même chose ;
- ça s'affiche **dans l'application**, au-dessus du champ de saisie — pas en
  notification qui sonne ;
- **« Jamais ça »** éteint ce genre de suggestion pour toujours, sans
  discussion ;
- tu peux tout couper dans ton profil (`non`, `discret`, `actif` — *discret*
  par défaut).

Répondre « oui » n'exécute rien tout seul : la phrase part **dans la
conversation**, comme si tu l'avais écrite, et Ydsan agit ensuite normalement.

### Les sujets que tu lui fais suivre

Tu peux lui demander de **suivre un sujet** : « surveille le prix des billets
pour Alger ». Il fait alors **une recherche par jour** sur ce sujet-là, en son
nom à lui — la requête part de la machine qui fait tourner Ydsan, pas de ton
téléphone.

Ce qu'il en garde : le **titre**, l'**extrait** et l'**adresse** du résultat,
tels que le moteur les a écrits. Rien n'est reformulé, rien n'est résumé,
aucun modèle n'intervient — c'est ce qui garantit que la source est réelle.

- **Trois sujets au maximum**, et seulement ceux que tu as nommés. Ydsan ne
  met jamais un sujet sous surveillance de lui-même.
- Tu l'arrêtes quand tu veux ; ce qu'il avait trouvé reste consultable.
- Aucune information sur toi ne part dans la recherche : il cherche le sujet,
  pas toi.

### Envoyer un message hors d'Ydsan

Quand tu lui demandes d'écrire à quelqu'un sur WhatsApp, par SMS ou par
courriel, il **ouvre l'application avec le message déjà écrit**. Il ne l'envoie
pas : le bouton reste sous ton doigt. Rien ne quitte ton téléphone tant que tu
n'as pas appuyé.

### Ta voix

Quand tu parles à Ydsan, l'enregistrement est envoyé pour être transcrit, puis
**oublié**. Il n'est écrit sur aucun disque, ni chez toi ni chez le service. Ce
qui reste, c'est le texte de ta phrase, comme si tu l'avais tapée.

### Où tout cela vit

Sur un hébergement **Supabase** (PostgreSQL) et sur la machine qui fait tourner
Ydsan. Les échanges passent par HTTPS. Les documents que tu fais fabriquer
restent sur la machine qui les a produits et sont effacés après un temps borné.

---

## 3. Ce qui n'est jamais lu

C'est aussi important que le reste.

- **Les contacts de ton téléphone.** Ceux de la messagerie sont ceux que tu
  crées toi-même dans l'application.
- **Ton agenda système**, celui de Google ou d'Apple. L'agenda d'Ydsan est le
  sien, et il ne contient que ce que tu y mets.
- **Tes photos, tes SMS, tes appels, ta position.**
- **La liste des applications installées.** L'application Android sait les
  ouvrir par leur nom, et cette recherche se fait **sur ton téléphone** : la
  liste ne part nulle part. Ce que quelqu'un installe en dit long sur lui —
  sa banque, sa religion, sa santé — et ça ne regarde personne d'autre.

---

## 4. Les permissions de l'application Android

Chacune sert à une chose précise, et à rien d'autre.

- **Micro** — parler à Ydsan. L'enregistrement n'est pas conservé.
- **Notifications** — te dire tes rappels et tes messages reçus.
- **Alarmes exactes** — faire sonner un réveil *à l'heure*. Sans elles, Android
  s'autorise un quart d'heure de retard.
- **Exemption de batterie** — ne pas être mis en veille par le système. Sans
  elle, le réveil ne sonne pas la nuit.
- **Voir les applications installées** — ouvrir celle que tu demandes par son
  nom. La liste reste sur l'appareil.
- **Démarrage** — reprogrammer les réveils après un redémarrage du téléphone.

---

## 5. L'amélioration du service — et ton accord

Ydsan peut garder une copie de tes échanges pour être réentraîné et mieux
répondre. **Cela ne se fait que si tu l'as accepté**, dans tes réglages, et
c'est **désactivé par défaut**.

Trois précisions honnêtes :

1. **L'accord vaut au moment de l'échange.** Si tu actives le partage
   aujourd'hui, ce que tu as dit hier n'est pas repris.
2. **Le couper arrête la collecte pour la suite.** Ce qui a déjà été copié
   avant que tu le coupes reste dans le jeu de données.
3. **Supprimer une conversation ne retire pas la copie déjà exportée.** Si tu
   veux qu'elle disparaisse aussi de là, demande-le à l'adresse de contact :
   c'est fait à la main.

Ces copies ne contiennent **ni courriel, ni jeton, ni mot de passe, ni
empreinte** — seulement les phrases échangées et un identifiant de compte.

---

## 6. Ce qui n'est jamais fait

- Tes données ne sont **ni vendues, ni louées, ni partagées** avec un tiers.
- Le contenu de tes extensions n'est **jamais** relu, agrégé ni réutilisé pour
  autre chose que te l'afficher et permettre à ton agent d'y écrire.
- Aucune publicité, aucun profilage publicitaire, aucun traceur.
- Aucun échange n'est lu pour autre chose que te répondre — et, si tu l'as
  accepté, pour améliorer le service.

---

## 7. Tes droits

Conformément au RGPD :

- **Accès** — voir tout ce qui est gardé sur toi.
- **Rectification** — corriger ton profil, ton nom, tes réglages, à tout moment
  dans l'application.
- **Effacement** — supprimer une conversation depuis l'application, ou demander
  la suppression complète de ton compte et de tout ce qui s'y rattache.
- **Portabilité** — recevoir tes échanges dans un format lisible.
- **Opposition** — couper le partage pour l'amélioration, sans perdre l'accès
  au service.

Pour l'effacement complet ou la portabilité : **contact.ydsan@gmail.com**.
Réponse sous trente jours.

---

## 8. Ce qu'Ydsan ne remplace pas

Ydsan est un logiciel, et il se trompe. Il ne remplace **ni un médecin, ni un
avocat, ni un savant en religion, ni un conseiller financier**. Sur ces
sujets-là, il dit ce qu'il sait avec prudence, dit clairement quand il n'est pas
sûr, et te renvoie à quelqu'un de compétent.

Il ne prétend pas non plus avoir fait une chose qu'il n'a pas faite : quand un
outil échoue, il le dit.

---

## 9. Changements

Ce texte change avec l'application. La version et la date en haut disent
laquelle tu lis. Les modifications importantes sont annoncées dans
l'application avant de s'appliquer.

---

## 10. Le service

Ydsan est un service personnel, fourni tel quel, sans garantie de disponibilité
continue : il tourne sur une machine qui peut être éteinte. Un compte peut être
fermé en cas d'usage manifestement abusif — spam, tentative d'accès aux données
d'autrui, contenu illégal.

*Dernière mise à jour : 6 septembre 2026 (2.3).*

# Conditions d'utilisation et politique de confidentialité

**Ydsan** — assistant personnel
Version 2.0 — 5 septembre 2026
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
documents et images fabriqués à ta demande. Ils t'appartiennent, et **toi seul**
les lis : la base refuse une lecture qui ne vient pas de ton compte
(*Row Level Security*), ce n'est pas une promesse mais une règle appliquée par
le moteur de base de données.

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

*Dernière mise à jour : 5 septembre 2026.*

# Simulateur d'épargne ETF

Simulateur web **autonome** — un seul fichier HTML, zéro dépendance, aucune donnée envoyée — pour visualiser ce que peut devenir une épargne investie en ETF : phase d'accumulation, fiscalité française, puis rente à la retraite.

Pensé pour un **public non initié** : bloc d'introduction pédagogique, aide contextuelle sur chaque champ, conseils personnalisés.

## Fonctionnalités

- **Accumulation** : capital initial, versements mensuels / trimestriels / annuels, indexation des versements sur l'inflation
- **Intérêts composés, frais et inflation** : TER de l'ETF, frais d'enveloppe, valeur réelle en pouvoir d'achat d'aujourd'hui
- **Fiscalité française simplifiée** : PEA, assurance-vie, CTO (flat tax 30 %), ou aucune — avec comparaison automatique de l'enveloppe la plus avantageuse
- **Phase de rente (décumulation)** — trois modes :
  - **Tout consommer** : rente maximale, capital épuisé exactement à l'espérance de vie (rien à transmettre)
  - **Rente fixe** : montant imposé, le simulateur indique jusqu'à quel âge le capital tient
  - **Règle des 4 %** : retrait annuel réputé soutenable, capital plutôt préservé (transmissible)
- **Objectif inversé** : calcule le versement nécessaire pour atteindre un capital ou une rente nette cible
- **Comparaison de 3 scénarios** de rendement (pessimiste / central / optimiste)
- **Partage par lien** : tous les paramètres sont encodés dans l'URL (idéal pour diffuser un scénario pré-configuré)
- Graphique interactif (canvas) avec info-bulles, tableau année par année, conseils personnalisés

## Utilisation

Ouvrir `index.html` dans un navigateur. C'est tout : pas de build, pas de serveur, pas d'installation.

Pour partager un scénario : régler les paramètres, cliquer sur **« Copier le lien »**, diffuser l'URL.

## Comment ça marche

- Un seul fichier `index.html` (HTML + CSS + JavaScript vanilla, graphique en canvas)
- Capitalisation mensuelle : le taux annuel est converti en taux mensuel équivalent, frais déduits
- À la retraite, chaque retrait est taxé au prorata de la part de plus-value contenue dans le capital (comme en pratique)
- Rente « tout consommer » résolue par dichotomie : le retrait mensuel maximal tel que le solde à l'espérance de vie soit nul

## Limites (simplifications assumées)

- Âge des enveloppes PEA / assurance-vie figé au départ à la retraite (les seuils de 5 et 8 ans n'évoluent plus pendant la décumulation)
- Assurance-vie : abattement de 4 600 €/an (personne seule) et taux unique ~24,7 % (seuil de 150 k€ de versements ignoré)
- L'objectif « capital cible » est résolu sur le capital **brut** (avant impôt)
- Rendements constants : pas de volatilité ni de hasard, c'est un outil de projection, pas de prévision

## Avertissement

Outil **éducatif**, à visée pédagogique — ce n'est pas un conseil en investissement. Les rendements passés ne préjugent pas des rendements futurs ; un investissement en actions comporte un risque de perte en capital. La fiscalité est simplifiée et peut évoluer. Vérifiez votre situation auprès d'un professionnel.



## Licence

MIT — © 2026 Stéphane Dorlac

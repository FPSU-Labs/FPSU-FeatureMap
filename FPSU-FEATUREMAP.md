# FPSU FeatureMap

## Intention

Centraliser les primitives et les composants de l'application pour qu'une modification de leur définition commune se propage partout où ils sont utilisés.

## Définition

Une feature est une capacité identifiable du logiciel qui répond à un besoin.

## Organisation

Placer le dossier `FeatureMap` à la racine du projet.

Le dossier contient :
- **Un Markdown.** Direction artistique et carte des features, avec les liens vers les primitives et composants.
- **Les primitives.** Les variables communes utilisées par l'application.
- **Les composants.** Leur code partagé, utilisé par l'application sans duplication.

## Instructions

- **Avant une nouvelle feature.** Consulter la direction artistique et les primitives et composants existants.
- **Ajouts visuels.** Réutiliser l'existant par défaut. Ne créer un nouvel élément que si sa nécessité est évidente ou sa création explicitement demandée, puis l'ajouter à la carte.
- **Lorsqu'un composant est modifié.** Vérifier qu'il utilise les définitions communes de la feature map. Sinon, le remplacer par l'existant adapté ou, seulement si nécessaire et justifié, intégrer sa définition dans la feature map et l'utiliser depuis celle-ci.

## Mise à jour

Mettre à jour la feature map lorsqu'un changement touche :

- **Direction artistique.** Le style recherché ou les références visuelles.
- **Primitives.** L'ajout, la modification ou la suppression d'une variable commune.
- **Composants.** L'ajout, la modification ou la suppression d'un composant réutilisable.
- **Features.** L'ajout, la modification ou la suppression d'une fonctionnalité, de son apparence ou de son comportement.
- **Liens avec le code.** Le nom ou l'emplacement des éléments référencés, ou les primitives et composants qu'ils utilisent. Mettre immédiatement à jour leurs références dans la feature map lorsqu'une variable ou un composant est renommé.

Supprimer immédiatement les informations périmées ou contradictoires.

## Format de la feature map

- **Direction artistique.** Le style recherché, les références visuelles et le rôle des couleurs dans cette identité.
- **Primitives.** Les valeurs communes, palette de couleurs, tailles, espacements, arrondis et typographie. Leurs variables sont définies une seule fois dans les fichiers de code du dossier `FeatureMap`, utilisés par l'application. La carte indique leur nom et leur emplacement. Modifier une variable modifie tous les éléments qui l'utilisent.
- **Composants.** Les pièces réutilisables construites avec ces primitives, regroupées dans le dossier `FeatureMap` et utilisées par leur nom sans recopier leur code. La carte indique leur nom et l'emplacement de leur définition dans le code. Modifier cette définition modifie toutes les utilisations du composant.
- **Features.** La liste complète de toutes les features de la codebase, organisée par grand domaine, feature et sous-feature. Ce que chaque fonctionnalité permet de faire et, si elle possède une interface, les composants qu'elle utilise, leur disposition et leur comportement visuel. Référencer les primitives et composants utilisés par leur nom exact dans le code.
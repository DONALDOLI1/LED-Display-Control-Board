# LED Display Control Board

<div align="center">

### OLITECH · Conception d'une carte de commande pour affichage LED

![Project](https://img.shields.io/badge/Project-Electronic%20Design-blue)
![Logic](https://img.shields.io/badge/Logic-Hardwired%20Logic-orange)
![Controller](https://img.shields.io/badge/Control-NE555%20%2B%20CD4015-green)
![CAD](https://img.shields.io/badge/CAD-KiCad-blue)
![PCB](https://img.shields.io/badge/PCB-Photochemical%20Fabrication-success)
![Documentation](https://img.shields.io/badge/README-FR%20%7C%20EN-lightgrey)

**Conception électronique · Conception PCB · Fabrication du circuit imprimé**

</div>

---

# 🇫🇷 VERSION FRANÇAISE

## 1. Présentation du projet

Le projet **LED Display Control Board** consiste à concevoir une carte électronique destinée à commander un affichage lumineux séquentiel présentant le message :

**« BIENVENUE EN GESI 3 »**

Cette carte a été conçue à la demande d'un groupe d'étudiants de la promotion inférieure. Le dispositif avait pour objectif de réaliser un affichage lumineux représentant leur promotion.

La conception électronique repose sur une architecture à logique câblée, sans utilisation de microcontrôleur. Elle permet de commander progressivement les différents caractères du message selon une séquence cumulative, suivie d'une remise à zéro automatique.

## 2. Objectifs du projet

Les principaux objectifs de cette conception sont :

- Concevoir une carte électronique capable de piloter un affichage LED séquentiel.
- Mettre en œuvre une architecture à logique câblée.
- Générer un signal d'horloge à l'aide d'un NE555 configuré en mode astable.
- Utiliser des registres à décalage CD4015 montés en cascade.
- Assurer la commande des sorties lumineuses à travers des transistors BC547.
- Concevoir et fabriquer le circuit imprimé correspondant.

## 3. Principe de fonctionnement

Le fonctionnement de la carte repose sur plusieurs étapes :

1. **Génération de l'horloge :** le NE555, configuré en mode astable, produit des impulsions périodiques.
2. **Commande séquentielle :** les impulsions d'horloge cadencent les registres à décalage CD4015 montés en cascade.
3. **Allumage cumulatif :** les caractères du message s'allument progressivement. Chaque nouveau caractère activé reste allumé pendant l'activation des suivants.
4. **Affichage complet :** lorsque le message « BIENVENUE EN GESI 3 » est entièrement affiché, il reste visible pendant une durée déterminée.
5. **Remise à zéro automatique :** un circuit de temporisation utilisant un condensateur intervient pour déclencher la remise à zéro des registres.
6. **Redémarrage du cycle :** toutes les sorties reviennent à leur état initial et une nouvelle séquence commence automatiquement.

Ce fonctionnement permet d'obtenir un affichage répétitif et automatique du message.

## 4. Architecture électronique

La carte est organisée autour de plusieurs fonctions électroniques complémentaires.

| Composant | Fonction principale |
|---|---|
| NE555 | Génération du signal d'horloge en mode astable |
| CD4015 | Registres à décalage pour la commande séquentielle |
| BC547 | Étages de commande des sorties lumineuses |
| Condensateur du circuit de temporisation | Participation à la temporisation et à la remise à zéro |
| Alimentation 12 V | Alimentation de la carte |
| Interrupteur | Mise sous tension et arrêt du système |
| LED témoin | Indication de présence de l'alimentation |

## 5. Conception électronique et PCB

La conception de la carte a été réalisée avec **KiCad**.

Les travaux effectués comprennent :

- Élaboration du schéma électronique.
- Organisation et interconnexion des composants.
- Affectation des empreintes.
- Implantation des composants sur le circuit imprimé.
- Routage des pistes électroniques.
- Préparation des fichiers nécessaires à la fabrication du PCB.

## 6. Fabrication du circuit imprimé

Après la conception numérique, le PCB a été fabriqué par un procédé **photochimique**.

Les principales opérations réalisées sont :

- Préparation et impression du typon.
- Insolation de la plaque photosensible.
- Révélation de la couche photosensible.
- Gravure du circuit imprimé.
- Obtention du PCB après traitement.

**Remarque :** les travaux présentés concernent la conception électronique et la fabrication physique du circuit imprimé. L'assemblage des composants et les essais du système complet n'ont pas été réalisés par le concepteur de la carte.

## 7. Outils et technologies

| Outil / Technologie | Utilisation |
|---|---|
| KiCad | Conception du schéma électronique et du PCB |
| NE555 | Génération d'horloge |
| CD4015 | Registres à décalage |
| BC547 | Commande des sorties |
| Procédé photochimique | Fabrication du circuit imprimé |

## 8. Galerie de conception 3D

Cette section présente les différentes vues de la conception électronique et du circuit imprimé réalisées sous KiCad.

*Les vues 3D et captures de conception seront ajoutées dans le dossier `3D_DESIGN/`.*

## 9. Galerie de réalisation

Cette galerie présentera les photographies du circuit imprimé obtenu après les différentes étapes de fabrication.

*Les photographies du PCB fabriqué seront ajoutées dans le dossier `REALIZATION/`.*

## 10. Documentation technique

Les documents techniques associés au projet seront regroupés dans le dossier `documents/`.

| Document | Description |
|---|---|
| Schéma électronique | Schéma complet de la carte |
| Plan d'implantation | Positionnement des composants |
| Typon | Support de fabrication du circuit imprimé |

## 11. État du projet

| Étape | État |
|---|---|
| Conception du schéma électronique | Réalisée |
| Conception et routage du PCB | Réalisés |
| Fabrication photochimique du PCB | Réalisée |
| Assemblage des composants | Non réalisé par le concepteur |
| Essais du système complet | Non réalisés par le concepteur |

---

# 🇬🇧 ENGLISH VERSION

## 1. Project Overview

The **LED Display Control Board** project involves the design of an electronic board intended to control a sequential LED display showing the message:

**"BIENVENUE EN GESI 3"**

The board was designed at the request of a group of students from the junior academic cohort. The device was intended to provide a luminous display representing their academic cohort.

The electronic design is based on a hardwired logic architecture, without using a microcontroller. It progressively controls the characters of the message through a cumulative lighting sequence followed by an automatic reset.

## 2. Project Objectives

The main objectives are:

- Design an electronic board for sequential LED display control.
- Implement a hardwired logic architecture.
- Generate clock pulses using an NE555 configured in astable mode.
- Use cascaded CD4015 shift registers.
- Drive the output stages through BC547 transistors.
- Design and manufacture the corresponding printed circuit board.

## 3. Operating Principle

The system operates through the following sequence:

1. **Clock generation:** the NE555 generates periodic clock pulses in astable mode.
2. **Sequential control:** the clock pulses drive the cascaded CD4015 shift registers.
3. **Cumulative lighting:** the display characters are progressively activated, while previously activated characters remain illuminated.
4. **Complete display:** once the entire message is displayed, it remains visible for a predetermined period.
5. **Automatic reset:** a timing circuit involving a capacitor triggers the reset of the registers.
6. **Cycle restart:** all outputs return to their initial state and the sequence starts again.

## 4. Electronic Architecture

| Component | Main Function |
|---|---|
| NE555 | Astable clock signal generation |
| CD4015 | Shift registers for sequential control |
| BC547 | Output switching stages |
| Timing capacitor | Timing and reset circuit |
| 12 V power supply | Board power supply |
| Switch | System ON/OFF control |
| Indicator LED | Power presence indication |

## 5. Electronic Design and PCB Development

The electronic design was carried out using **KiCad**.

The work included:

- Electronic schematic design.
- Component organization and interconnection.
- Footprint assignment.
- PCB component placement.
- PCB track routing.
- Preparation of PCB manufacturing files.

## 6. Printed Circuit Board Fabrication

After the digital design stage, the PCB was manufactured using a **photochemical process**.

The main fabrication steps included:

- Artwork preparation and printing.
- Photosensitive board exposure.
- Developing.
- Chemical etching.
- Obtaining the fabricated PCB.

**Note:** This project covers the electronic design and physical fabrication of the printed circuit board. Component assembly and complete system testing were not performed by the board designer.

## 7. Tools and Technologies

| Tool / Technology | Application |
|---|---|
| KiCad | Electronic schematic and PCB design |
| NE555 | Clock generation |
| CD4015 | Shift registers |
| BC547 | Output control |
| Photochemical process | PCB fabrication |

## 8. 3D Design Gallery

This section presents the different views of the electronic design and printed circuit board created using KiCad.

*3D views and design screenshots will be added to the `3D_DESIGN/` directory.*

## 9. Fabrication Gallery

This section presents photographs of the printed circuit board obtained after the fabrication process.

*Photographs of the fabricated PCB will be added to the `REALIZATION/` directory.*

## 10. Technical Documentation

Technical documents, including the electronic schematic, component layout and PCB artwork, will be organized in the `documents/` directory.

| Document | Description |
|---|---|
| Electronic Schematic | Complete electronic circuit |
| Component Layout | Component placement |
| PCB Artwork | Printed circuit board manufacturing artwork |

## 11. Project Status

| Stage | Status |
|---|---|
| Electronic schematic design | Completed |
| PCB design and routing | Completed |
| Photochemical PCB fabrication | Completed |
| Component assembly | Not performed by the designer |
| Complete system testing | Not performed by the designer |

---

<div align="center">

### OLITECH

**Electronics · Embedded Systems · PCB Design**

*Designing practical electronic solutions.*

</div>

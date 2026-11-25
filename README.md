# dragster_base
it sti2d

# Mini-Projet STI2D : Dragster Motorisé

**Concevoir pour gagner** — Réalisation d'un dragster motorisé à courroie destiné à des courses en duel sur piste rectiligne[cite: 1, 2, 25].

---

## Présentation et règlement de la compétition

L'objectif du projet est de concevoir et fabriquer un dragster motorisé capable de remporter des duels sur une piste droite de **4 à 12 mètres**[cite: 2].

* **Départ :** À l'arrêt au signal, en lâchant simplement le véhicule sans aucune aide extérieure.
* **Victoire :** Franchir la ligne d'arrivée en premier tout en restant dans sa voie (`1 point`).
* **Sortie de piste :** Élimination immédiate sur la manche (si les deux concurrents sortent, celui qui a parcouru la plus grande distance remporte `0,5 point`)[cite: 2].

---

## Équipe et répartition des rôles

* **Chef de projet :** Noah
* **Membres de l'équipe :** Noah, Mathys (et Fatima / Ilan selon les phases)
* **Organisation des étapes :**
  * *Temps 1 — Implantation :* Meneur Noah / Participant Mathys
  * *Temps 2 — Groupe de propulsion :* Meneur Mathys / Participant Noah
  * *Temps 3 & 4 — Essieu avant & Carrosserie :* Conception collective[cite: 1, 3, 7, 24, 25, 26]

---

## Caractéristiques techniques et choix de conception

### 1. Châssis et architecture (Implantation)
* **Matériaux :** Châssis en PVC (6 mm, dimensions 50 × 200 mm), axes en acier (3 mm), roues en ABS munies de bandages élastiques pour l'adhérence, carrosserie en polypropylène.
* **Répartition des masses :** Piles placées au centre et moteur reculé à l'arrière afin d'obtenir un centre de gravité bas et légèrement arrière, maximisant la motricité sans délester l'avant[cite: 28, 30, 31, 33].

### 2. Transmission et propulsion
* **Chaîne d'énergie :** 3 piles R6 (4,5 V) -> Interrupteur / Carte DGB -> Moteur D21 -> Poulie motrice -> Courroie -> Poulie réceptrice -> Axe arrière -> Roues.
* **Configuration retenue (compromis couple / vitesse) :**
  * Poulie moteur : **10 mm**
  * Poulie réceptrice : **34 mm** (rapport de réduction de `0,2941`, soit environ `3 824 tr/min` à la roue pour un moteur à `13 000 tr/min`)
  * Roues arrière : **60 mm** avec bandage[cite: 23, 28, 34, 35, 37]

### 3. Aérodynamisme
* **Forme retenue :** Profil ovoïde / pisciforme (nez arrondi, section frontale réduite, arrière effilé) pour limiter la traînée aérodynamique ($F_D = \frac{1}{2} \rho \cdot C_D \cdot S \cdot v^2$) et éviter le soulèvement du véhicule[cite: 3, 4].

### 4. Électronique et programmation
* **Contrôleur :** Carte DGB (Picaxe 08M2) alimentée en 4,5 V, pilotant le moteur par signal **PWM** (modulation de largeur d'impulsion).
* **Logique embarquée :** Programmation sous **Blockly** intégrant une **loi

# TP4 – Java SE : Principes de la POO

**Module :** ID1 – S2 / 2025-26  
**École :** ENSA Al Hoceima – Université Abdelmalek Essaâdi  
**Encadrant :** Pr. Mohamed CHERRADI

---

## 📋 Objectif

Ce TP a pour objectif de comprendre et mettre en pratique les principes fondamentaux de la **Programmation Orientée Objet (POO)** en Java :

- Héritage
- Polymorphisme
- Classes abstraites
- Interfaces

---

## 📁 Structure du projet

```
TP4_java/
│
├── exercice1/
│   ├── Personne.java
│   └── Etudiant.java
│
├── exercice2/
│   ├── Vehicule.java
│   └── Voiture.java
│
├── exercice3/
│   ├── Compte.java
│   ├── CompteCourant.java
│   └── CompteEpargne.java
│
├── exercice4/
│   ├── Animal.java
│   ├── Chien.java
│   └── Chat.java
│
├── exercice5/
│   ├── Figure.java
│   ├── Cercle.java
│   └── Triangle.java
│
├── exercice7/
│   ├── Forme.java        ← classe abstraite
│   ├── Rectangle.java
│   └── Cercle.java
│
├── exercice8/
│   ├── Volant.java       ← interface
│   ├── Oiseau.java
│   └── Avion.java
│
├── exercice9/
│   ├── Vehicule.java     ← classe abstraite
│   ├── Electrique.java   ← interface
│   ├── VoitureElectrique.java
│   └── Moto.java
│
└── exercice10/
    ├── Document.java         ← classe abstraite
    ├── Empruntable.java      ← interface
    ├── Consultable.java      ← interface
    ├── Livre.java
    ├── Magazine.java
    ├── DocumentNumerique.java
    └── Utilisateur.java
```

---

## 📝 Description des exercices

### Exercice 1 – Héritage : Personne & Étudiant
Modélisation d'un système académique.
- `Personne` : attributs `nom`, `prénom`, `âge` + méthodes `afficherInformations()`, `estMajeur()`, `sePresenter()`
- `Etudiant` hérite de `Personne` : ajoute `niveau`, `moyenne` + méthodes `calculerMention()`, `estAdmis()`, `afficherProfil()`

### Exercice 2 – Constructeur implicite vs explicite : Véhicules
Illustration de l'importance des constructeurs dans une hiérarchie.
- `Vehicule` : attribut `marque` + méthodes `afficherMarque()`, `demarrer()`, `arreter()`
- `Voiture` hérite de `Vehicule` : ajoute `nbPortes`, `carburant` + méthodes `afficherDetails()`, `klaxonner()`
- Comparaison du comportement **avec** et **sans** appel explicite à `super()`

### Exercice 3 – Héritage : Système bancaire
- `Compte` : attribut `solde` + méthodes `deposer()`, `retirer()`, `consulterSolde()`, `afficher()`
- `CompteCourant` : ajoute `autoriserDecouvert()`, `calculerFrais()`
- `CompteEpargne` : ajoute `calculerInterets()`, `ajouterInterets()`
- Redéfinition de `afficher()` dans chaque sous-classe

### Exercice 4 – Polymorphisme : Animaux
- `Animal` : méthodes `crier()`, `manger()`, `dormir()`
- `Chien` : redéfinit `crier()` + ajoute `garder()`, `jouer()`
- `Chat` : redéfinit `crier()` + ajoute `ronronner()`, `grimper()`
- Mise en évidence du polymorphisme dynamique

### Exercice 5 – Polymorphisme : Figures géométriques
- `Figure` : méthodes `dessiner()`, `deplacer(x,y)`, `redimensionner(facteur)`
- `Cercle` et `Triangle` : redéfinissent `dessiner()` + ajoutent `calculerPerimetre()`, `calculerSurface()`

### Exercice 7 – Classe abstraite : Formes géométriques
- `Forme` (abstraite) : méthode abstraite `calculerSurface()` + méthodes concrètes `afficherDescription()`, `comparerSurface(Forme f)`
- `Rectangle` et `Cercle` : implémentent `calculerSurface()`, `calculerPerimetre()`, `validerDimensions()`

### Exercice 8 – Interface : Entités volantes
- Interface `Volant` : méthodes `voler()`, `atterrir()`, `changerAltitude()`
- `Oiseau` : implémente `Volant` + ajoute `migrer()`, `construireNid()`
- `Avion` : implémente `Volant` + ajoute `embarquerPassagers()`, `afficherAltitude()`

### Exercice 9 – Héritage + Interface + Abstraction : Véhicules modernes
- `Vehicule` (abstraite) : attribut `vitesse` + méthodes `accelerer()`, `freiner()` + méthode abstraite `demarrer()`
- Interface `Electrique` : méthodes `charger()`, `verifierBatterie()`
- `VoitureElectrique` : étend `Vehicule` + implémente `Electrique` + ajoute `afficherAutonomie()`, `optimiserConsommation()`
- `Moto` : étend `Vehicule` + ajoute `faireRoueArriere()`, `afficherTypeMoto()`

### Exercice 10 – Cas d'étude : Bibliothèque numérique
Système complet de gestion de documents.
- `Document` (abstraite) : attributs `id`, `titre`, `auteur`, `disponible` + méthode abstraite `calculerDureeEmpruntMax()`
- Interfaces : `Empruntable` (`estDisponible()`, `reserver()`) et `Consultable` (`consulter()`, `afficherResume()`)
- `Livre` hérite de `Document` + implémente `Empruntable`
- `Magazine` hérite de `Document` + implémente `Empruntable`
- `DocumentNumerique` hérite de `Document` + implémente `Consultable`
- `Utilisateur` : gestion des emprunts et historique
- Fonctionnalités : recherche, filtrage, documents populaires, gestion des pénalités

---

## ⚙️ Prérequis

- Java JDK 8 ou supérieur
- Un IDE Java (IntelliJ IDEA, Eclipse, VS Code...)
- Git (pour la gestion de version)

---

## 🚀 Compilation & Exécution

```bash
# Compiler un exercice (exemple : exercice1)
javac exercice1/*.java

# Exécuter la classe principale
java exercice1.Main
```

---

## 📦 Rendu

- Travail **individuel**
- Compresser tous les fichiers dans une archive : `Nom-Prenom.zip`
- Envoyer par e-mail à : **mcherradi.ensah@gmail.com**
- Objet du mail : `TP4-JSE`

---

## 🔑 Concepts clés abordés

| Concept | Exercices |
|---|---|
| Héritage (`extends`) | 1, 2, 3, 9, 10 |
| Polymorphisme | 4, 5, 10 |
| Classe abstraite (`abstract`) | 7, 9, 10 |
| Interface (`interface`) | 8, 9, 10 |
| Surcharge de méthodes (`@Override`) | 3, 4, 5, 7, 10 |
| Appel au constructeur parent (`super`) | 1, 2 |

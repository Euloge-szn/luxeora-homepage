# LUXEORA Fashion House 🏛️



> \*\*L'élégance intemporelle, désormais à portée de clic.\*\*



!\[HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat\&logo=html5\&logoColor=white)

!\[CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat\&logo=css3\&logoColor=white)

!\[Responsive](https://img.shields.io/badge/Responsive-Design-gold)

!\[Status](https://img.shields.io/badge/Status-En%20production-brightgreen)



---



\## 📌 Présentation du projet



\*\*LUXEORA Fashion House\*\* est une page d'accueil professionnelle réalisée dans le cadre du \*\*Bloc 1 – Développement Web\*\* du Parcours L1 IFRI de l'Académie de Programmation.



Ce projet simule la transformation digitale d'une boutique de mode haut de gamme spécialisée dans les collections homme et femme. Face à une baisse progressive de ses performances commerciales liée à une présence digitale insuffisante, LUXEORA a décidé de lancer sa première vitrine web professionnelle.



---



\## 🧩 Problématique Business



LUXEORA rencontrait les difficultés suivantes avant ce projet :



\- Absence totale de site web officiel

\- Dépendance excessive aux réseaux sociaux

\- Image de marque vieillissante et incohérente

\- Faible taux de conversion des visiteurs en clients

\- Aucune collecte de données clients

\- Trafic uniquement physique en boutique



\*\*Solution apportée :\*\* Une page d'accueil moderne, élégante et optimisée, conçue pour renforcer la visibilité de la marque, améliorer son image et stimuler les ventes en ligne.



---



\## 🗂️ Structure du projet



```

LUXEORA Fashion House/

│

├── index.html          → Page principale (structure HTML5 sémantique)

├── style.css           → Feuille de style externe (CSS3)

├── README.md           → Documentation du projet

│

└── assets/

&nbsp;   ├── image/

&nbsp;   │   ├── femme1.jpg … femme8.jpg   (Collection Femme)

&nbsp;   │   └── homme1.jpg … homme7.jpg  (Collection Homme)

&nbsp;   └── logo/

&nbsp;       └── logo.jpeg                 (Logo officiel LUXEORA)

```



---



\## 📄 Sections de la page



| # | Section | Description |

|---|---------|-------------|

| 1 | \*\*Header\*\* | Logo, navigation desktop, burger mobile, bouton mode sombre/clair, ticker d'annonces |

| 2 | \*\*Hero\*\* | Image pleine page, titre impactant, statistiques clés, call-to-action |

| 3 | \*\*Bandeau Message Fort\*\* | Défilement animé — \*"L'élégance intemporelle, désormais à portée de clic"\* |

| 4 | \*\*Produits Phares\*\* | 4 pièces iconiques avec catégorie, nom et prix |

| 5 | \*\*Galerie\*\* | Carrousel horizontal scroll-snap avec 6 visuels de saison |

| 6 | \*\*À propos\*\* | Histoire de la marque, valeurs, images empilées, badge 14 ans |

| 7 | \*\*Promotions\*\* | Soldes −40%, compte à rebours, Capsule Dorée, Cercle Prestige |

| 8 | \*\*Témoignages\*\* | 4 avis clients de taille uniforme |

| 9 | \*\*Newsletter VIP\*\* | Formulaire d'inscription au Cercle Privé LUXEORA |

| 10 | \*\*Footer\*\* | Logo, liens utiles, réseaux sociaux, informations de contact |



---



\## ⚙️ Techniques CSS avancées utilisées



\### 🎨 Thème Clair / Sombre — CSS `:checked` Hack

Aucun JavaScript. Le basculement de thème est réalisé uniquement avec :

\- Un `<input type="checkbox" id="theme-toggle">` caché

\- Le sélecteur CSS `.theme-input:checked ~ .page-wrap` qui redéfinit toutes les variables



```css

.theme-input:checked ~ .page-wrap {

&nbsp; --bg:   #0D0B09;

&nbsp; --text: #F0EAE0;

&nbsp; --gold: #C5A96A;

&nbsp; /\* ... \*/

}

```



\### 🍔 Menu Burger Mobile — CSS `:checked` Hack

Pareil, zéro JavaScript :

\- Un `<input type="checkbox" id="menu-toggle">` caché

\- Le menu mobile s'ouvre avec `max-height: 500px` via `:checked`



```css

.menu-input:checked ~ .page-wrap .mobile-nav {

&nbsp; max-height: 500px;

}

```



\### 📐 Typographie Fluide — `clamp()`

Toute la typographie s'adapte élastiquement à tous les écrans sans media queries multiples :



```css

.section-title { font-size: clamp(2.2rem, 5vw, 5rem); }

.ht-bold       { font-size: clamp(3rem, 8vw, 8rem);   }

.hero-sub      { font-size: clamp(0.8rem, 1.8vw, 0.92rem); }

```



\### 🎠 Galerie Carrousel — `scroll-snap-type`

La galerie utilise le défilement horizontal avec accrochage CSS natif :



```css

.snap-track {

&nbsp; scroll-snap-type: x mandatory;

&nbsp; overflow-x: auto;

}

.snap-card {

&nbsp; scroll-snap-align: start;

}

```



\### 📦 Mise en page — Flexbox

Toute la mise en page est réalisée avec \*\*Flexbox\*\* : header, grille produits, section about, promos, témoignages, footer.



\### 📱 Responsive Design

Adaptation complète via media queries à trois niveaux :

\- \*\*≤ 1100px\*\* — Tablette large

\- \*\*≤ 860px\*\*  — Tablette (burger activé, colonnes empilées)

\- \*\*≤ 560px\*\*  — Mobile (tout en colonne unique)



---



\## 🎨 Choix de design



| Élément | Choix | Justification |

|---------|-------|---------------|

| \*\*Direction artistique\*\* | Maison de Mode Éditoriale Lumineuse | Évoque le luxe accessible, clair et élégant |

| \*\*Police d'affichage\*\* | Cormorant Garamond | Haute couture, contrastes typographiques marqués |

| \*\*Police de corps\*\* | Josefin Sans | Géométrique, moderne, lisible à toutes tailles |

| \*\*Couleur principale\*\* | Ivoire chaud `#FAF8F3` | Fond lumineux, chaleureux, non agressif |

| \*\*Couleur accent\*\* | Or patiné `#9A7040` | Luxe sobre, non clinquant |

| \*\*Couleur sombre\*\* | Encre `#0D0B09` | Noir organique pour le mode sombre |



---



\## 🚀 Lancer le projet



1\. Cloner ou télécharger le dépôt

2\. Ouvrir le dossier `LUXEORA Fashion House/`

3\. Double-cliquer sur `index.html` ou utiliser \*\*VS Code Live Server\*\*

4\. ✅ Aucune installation requise — HTML \& CSS purs



---



\## ✅ Contraintes techniques respectées



\- \[x] HTML5 sémantique exclusivement

\- \[x] CSS3 avec feuille de style externe

\- \[x] Aucun JavaScript ni framework

\- \[x] Flexbox pour toute la mise en page

\- \[x] Responsive design (mobile, tablette, desktop)

\- \[x] `clamp()` pour la typographie fluide

\- \[x] `scroll-snap-type` pour la galerie

\- \[x] Thème sombre/clair via `:checked` CSS

\- \[x] Burger mobile via `:checked` CSS

\- \[x] Code indenté et organisé



---



\## 📊 Critères d'évaluation



| Critère | Poids |

|---------|-------|

| Qualité et structure HTML | 20% |

| Maîtrise du CSS et mise en page | 25% |

| Responsive design | 15% |

| Professionnalisme du design | 15% |

| Qualité du rapport écrit | 15% |

| Clarté et pertinence du Business Plan | 10% |



---



\## 👨‍💻 Auteur



\*\*Parcours L1 IFRI — Académie de Programmation\*\*  

Projet Académique · Bloc 1 Développement Web · 2025



---



> \*"L'élégance n'est pas un luxe, c'est un état d'esprit."\*  

> — LUXEORA Fashion House


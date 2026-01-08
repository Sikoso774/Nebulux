# 🌌 HUD Galaxy Theme for Obsidian

Un thème complet pour Obsidian inspiré des interfaces Sci-Fi (HUD), optimisé pour Windows 11.
Ce projet transforme l'éditeur de texte en véritable cockpit de vaisseau spatial avec des effets de transparence (Glassmorphism), des animations néons et une gestion sonore immersive.

![Graph View Screenshot](screenshot.png)

## 🚀 Fonctionnalités Clés

* **Glassmorphism Réel sur Windows :** Intégration avancée avec le moteur de rendu via *Pseudo Mica* pour contourner les limitations de transparence d'Electron sur Windows 11.
* **Système de Couleurs Cyclique :** Utilisation de `:nth-child` et de variables CSS (`var(--color-nav)`) pour colorer automatiquement les dossiers et l'interface sans intervention manuelle.
* **Graph View HUD :** Panneau de contrôle flottant entièrement transparent avec effets de flou (`backdrop-filter`) et accélération matérielle forcée (`transform: translateZ(0)`).
* **Soundscapes Integration :** Support natif pour les ambiances sonores via ID YouTube.

## 🛠️ Challenges Techniques & Solutions

### Le Bug du "Voile Gris" (Windows/Electron)

Sur Windows, l'accélération matérielle désactive souvent le `backdrop-filter` sur les éléments flottants au-dessus du WebGL (Graph View), créant un fond gris opaque lors du focus.

**Solution :**
J'ai implémenté un correctif CSS hybride qui force la création d'une nouvelle couche de composition GPU tout en utilisant le plugin *Pseudo Mica* pour gérer la transparence au niveau de la fenêtre OS.

```css
/* Extrait du code correctif */
.graph-controls {
    background-color: rgba(13, 17, 26, 0.60) !important;
    backdrop-filter: blur(12px);
    transform: translateZ(0); /* Force GPU Layer */
    will-change: transform, backdrop-filter;
}
```

## 📦 Installation

1. Téléchargez le fichier `theme.css`.
2. Placez-le dans `.obsidian/themes/HUD Galaxy Theme/`.
3. Activez le thème dans les paramètres d'Obsidian.
4. **Requis :** Installez le plugin "Style Settings" pour la configuration et "Pseudo Mica" pour la transparence.

## 🎨 Personnalisation

Le thème est entièrement configurable via des variables CSS exposées dans Style Settings :
-`--hud-blur`: Intensité du flou.
-`--color-nav`: Couleur principale (Défaut: Bleu Néon).

---
*Développé par Sikoso774*

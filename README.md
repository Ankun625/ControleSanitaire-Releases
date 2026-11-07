# Contrôle sanitaire – versions publiées

Ce dépôt contient **uniquement les versions publiées** (fichiers d'installation) des deux applications de contrôle sanitaire des établissements alimentaires (décret n° 2-10-473). Le code source n'est pas public.

| Application | Plateforme | Versions |
|---|---|---|
| **Contrôle sanitaire (bureau)** : import des inspections, fiches établissements, rapports PDF, exports Excel | Windows 10 / 11 (64 bits) | tags `bureau-vX.Y.Z` |
| **Inspection alimentaire** : formulaire d'inspection sur le terrain, non-conformités, saisies, photos, export | Android 8.0 ou plus récent | tags `android-vX.Y.Z` |

➡️ Toutes les versions sont dans l'onglet **[Releases](../../releases)**.

---

## Application bureau (Windows)

### Première installation
1. Ouvrez la dernière version `bureau-v…` dans **Releases**.
2. Téléchargez `ControleSanitaire_Setup_X.Y.Z.exe` et lancez-le.
3. Si Windows affiche « Windows a protégé votre ordinateur », cliquez sur **Informations complémentaires**, puis **Exécuter quand même**.
4. L'installation ne demande pas de droits administrateur.

### Mises à jour
L'application les recherche **au démarrage** et depuis **Paramètres → Mises à jour → Rechercher des mises à jour**. Une fois la mise à jour acceptée, l'application la télécharge, la vérifie, se ferme, s'installe puis se relance.

Les données (inspections, photos, paramètres) se trouvent dans `%LOCALAPPDATA%\ControleSanitaire`. Les mises à jour ne les modifient pas. À la désinstallation, elles sont conservées par défaut.

### Fichiers d'une version
| Fichier | Rôle |
|---|---|
| `ControleSanitaire_Setup_X.Y.Z.exe` | Programme d'installation |
| `manifest.json` | Description de la version (nom du fichier, taille, empreinte SHA-256) |
| `manifest.json.sig` | Signature numérique du manifeste |

---

## Application Android

### Première installation
1. Sur la tablette, ouvrez la dernière version `android-v…` dans **Releases**.
2. Téléchargez `InspectionAlimentaire-X.Y.Z.apk` et ouvrez-le.
3. Autorisez l'installation depuis cette source si Android le demande, puis confirmez.

### Mises à jour
L'application les recherche **au démarrage**. Vous pouvez aussi passer par le bouton **ⓘ** de l'écran d'accueil, puis **Rechercher maintenant**. Android demande toujours une confirmation avant d'installer. Les inspections enregistrées sur la tablette sont conservées.

---

## Sécurité
- Les applications se contentent de **lire** la liste des versions publiées ici. **Aucune donnée d'inspection n'est envoyée.**
- **Windows** : avant de lancer l'installation, l'application vérifie la signature de `manifest.json` avec une clé publique intégrée, puis l'empreinte SHA-256 et la taille du fichier téléchargé. Si un fichier a été modifié ou remplacé, il est refusé.
- **Android** : l'APK téléchargé doit être signé avec le même certificat que l'application installée et avoir un numéro de version plus élevé. Android lui-même refuse toute mise à jour signée par une autre clé.
- Ne renommez pas les fichiers d'une version et n'en ajoutez pas : les applications s'appuient sur leurs noms exacts.

## Support
Pour un problème d'installation ou de mise à jour, contactez le responsable informatique du service et indiquez la version installée. Elle est visible dans **Paramètres → Mises à jour** (Windows) ou via le bouton **ⓘ** (Android).

# 📱 Guide — Compiler l'APK École Virtuelle MSAR via GitHub Actions

## Ce que tu vas obtenir
Un APK Android qui ouvre **https://famous-pie-035cbf.netlify.app/** dans une WebView
native, avec :
- Barre de progression dorée pendant le chargement
- Page hors-ligne si pas de connexion
- Pull-to-refresh (glisser vers le bas pour recharger)
- Gestion du bouton Retour Android
- Upload de fichiers depuis le WebView
- Cookies et stockage persistants

---

## Étape 1 — Créer un compte GitHub (gratuit)
1. Va sur **https://github.com**
2. Clique **Sign up** → crée un compte gratuit

---

## Étape 2 — Créer un nouveau dépôt
1. Connecte-toi à GitHub
2. Clique le **+** en haut à droite → **New repository**
3. Nom : `EcoleVirtuelle` (ou ce que tu veux)
4. ✅ **Public** (obligatoire pour les Actions gratuites)
5. Clique **Create repository**

---

## Étape 3 — Uploader les fichiers du projet
1. Dans ton nouveau dépôt, clique **uploading an existing file** (ou **Add file** → **Upload files**)
2. **Dézippe** le fichier `EcoleVirtuelle_Android.zip` sur ton PC
3. **Glisse-dépose TOUS les fichiers et dossiers** dans la zone d'upload GitHub
   > ⚠️ Important : conserve la structure des dossiers !
4. En bas, clique **Commit changes**

---

## Étape 4 — Vérifier que le build se lance
1. Clique sur l'onglet **Actions** dans ton dépôt
2. Tu verras un workflow **"Build APK"** en cours (cercle jaune = en cours)
3. Attends ~5 minutes

---

## Étape 5 — Télécharger l'APK
1. Quand le workflow est ✅ vert, clique dessus
2. En bas de la page, section **Artifacts**, tu verras :
   - `EcoleVirtuelle-debug` ← **télécharge celui-ci**
   - `EcoleVirtuelle-release`
3. Clique pour télécharger → tu obtiens un `.zip` contenant l'APK

---

## Étape 6 — Installer l'APK sur Android
1. Transfère l'APK sur ton téléphone (USB, WhatsApp, email…)
2. Sur Android : **Paramètres** → **Sécurité** → activer **Sources inconnues**
   (ou selon ton Android : **Installer des apps inconnues**)
3. Ouvre le fichier APK → **Installer**

---

## ❓ Problèmes fréquents

| Problème | Solution |
|----------|----------|
| Build échoue (rouge) | Clique sur le build → lis les logs → contacte le support |
| "App not installed" | Désinstalle l'ancienne version d'abord |
| Écran blanc | Vérifie ta connexion internet |
| Upload GitHub lent | Compresse d'abord en ZIP et uploade le ZIP |

---

## 🔄 Mettre à jour l'APK
Si tu changes l'URL ou la config, modifie `MainActivity.java` ligne ~17 :
```java
private static final String APP_URL = "https://TON-URL.netlify.app/";
```
Puis commit → GitHub recompile automatiquement !

---

*Projet : École Virtuelle MADOUGOU SAR — APK v1.0*

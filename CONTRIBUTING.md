# 🤝 Guide de contribution

Merci de contribuer à ce projet ! 🎉  
Voici quelques règles pour assurer une collaboration fluide et respectueuse du flux de travail.

---

## 📌 Branches

- **`main`** est la branche de production.  
  **🔒 Aucun push direct n’est autorisé.**
- Crée une nouvelle branche pour chaque fonctionnalité ou correction de bug :

```bash
git checkout -b feat/nom-de-la-fonctionnalite
```

---

## 🛠️ Modifications

1. Ne jamais travailler directement sur `main`.
2. Commence sur une branche propre dérivée de `main`.
3. Une fois terminé, pousse ta branche :

```bash
git push origin feat/nom-de-la-fonctionnalite
```

4. Ouvre une **Pull Request (PR)** vers `main`.

---

## ✅ Revue de code

- Chaque PR doit être **reviewée et approuvée** par au moins un membre avant merge.
- Résous toutes les discussions/commentaires avant le merge.
- Tu peux demander une revue avec `@mention`.

---

## 🚫 Interdictions

- ❌ Pas de `git push` direct sur `main`
- ❌ Pas de merge sans PR
- ❌ Pas de commit sans message clair

---

## ✅ Bonnes pratiques

- Utilise des noms de branches clairs :  
  `feat/ajout-contact`, `fix/erreur-affichage`, `doc/update-readme`
- Commits lisibles et précis :
  ```bash
  git commit -m "feat: ajout du composant carte membre"
  ```

- Teste toujours tes modifications avant d’ouvrir une PR.
- Maintiens ton fork ou ta branche à jour avec `main` :
  ```bash
  git pull origin main --rebase
  ```

---

## 📬 Besoin d'aide ?

N'hésite pas à ouvrir une issue ou à contacter les maintainers.  
Merci pour ta contribution 🙌

---
# 🚀 Deployment zu GitHub Pages

## Schritt 1: Dateien ins Repository hochladen

```bash
# Wechsle in das Verzeichnis mit den Dateien
cd "C:\Users\D054019\OneDrive - SAP SE\Documents\GitHub\Github.com - privat\my-private-collection\lechbruck-github-pages"

# Initialisiere Git (falls noch nicht geschehen)
git init

# Füge das Remote Repository hinzu
git remote add origin https://github.com/EnTaroAdunExecutar/Lechbruck-guide.git

# Füge alle Dateien hinzu
git add .

# Erstelle den ersten Commit
git commit -m "🏔️ Initial commit: Lechbruck Reiseführer mit PWA-Features"

# Push zum GitHub Repository (main branch)
git branch -M main
git push -u origin main
```

---

## Schritt 2: GitHub Pages aktivieren

### Variante A: Über GitHub Website (Einfacher)

1. Gehe zu deinem Repository: https://github.com/EnTaroAdunExecutar/Lechbruck-guide

2. Klicke auf **Settings** (oben rechts)

3. Scrolle links runter zu **Pages** (unter "Code and automation")

4. Unter **Source**: Wähle **Deploy from a branch**

5. Unter **Branch**:
   - **Branch:** `main`
   - **Folder:** `/ (root)`

6. Klicke **Save**

7. **Warte 1-2 Minuten** - GitHub baut deine Seite

8. Refresh die Seite - oben erscheint:  
   "✅ Your site is live at https://entaroadunexecutar.github.io/Lechbruck-guide/"

---

### Variante B: Mit GitHub CLI (Optional)

```bash
# GitHub CLI installiert? Prüfe mit:
gh --version

# Falls ja, kannst du Pages so aktivieren:
gh repo edit --enable-pages --pages-branch main --pages-path /
```

---

## Schritt 3: Testen

Öffne in 1-2 Minuten:
```
https://entaroadunexecutar.github.io/Lechbruck-guide/
```

🎉 **Fertig!** Dein Reiseführer ist jetzt online!

---

## 📱 Bonus: Custom Domain (Optional)

Falls du eine eigene Domain hast (z.B. `lechbruck-guide.com`):

1. Erstelle eine Datei `CNAME` (ohne Endung!) mit folgendem Inhalt:
   ```
   deine-domain.com
   ```

2. Bei deinem Domain-Provider (z.B. Namecheap, GoDaddy):
   - Erstelle einen **A Record** zu:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Oder einen **CNAME Record** zu: `entaroadunexecutar.github.io`

3. In GitHub Settings → Pages:
   - Gib deine Custom Domain ein
   - Aktiviere "Enforce HTTPS"

---

## 🔄 Updates veröffentlichen

Wenn du später Änderungen machst:

```bash
# Ins Projektverzeichnis wechseln
cd "C:\Users\D054019\OneDrive - SAP SE\Documents\GitHub\Github.com - privat\my-private-collection\lechbruck-github-pages"

# Änderungen hinzufügen
git add .

# Commit mit Beschreibung
git commit -m "✨ Update: Neue Restaurants hinzugefügt"

# Push zu GitHub
git push origin main
```

**Automatisch** wird die Seite in 1-2 Minuten aktualisiert! 🚀

---

## 🐛 Troubleshooting

### Problem: Seite zeigt 404 Error

**Lösung:**
- Warte 2-3 Minuten nach dem ersten Push
- Prüfe: Settings → Pages → Branch muss auf `main` stehen
- Prüfe: `index.html` muss im Root-Verzeichnis liegen (nicht in Unterordner)

### Problem: Styles werden nicht geladen

**Lösung:**
- Öffne die Browser-Konsole (F12)
- Prüfe auf Fehler
- CSS ist inline in der HTML - sollte immer funktionieren!

### Problem: PWA Install-Button erscheint nicht

**Lösung:**
- Funktioniert nur über HTTPS (GitHub Pages hat das automatisch)
- Auf manchen Browsern nur nach 2. Besuch
- iOS Safari zeigt den Button nicht - nutze "Teilen → Zum Home-Bildschirm"

---

## 📊 Analytics (Optional)

Falls du Besucherzahlen tracken möchtest:

1. **Google Analytics:** Füge das Script in `<head>` ein
2. **Plausible Analytics:** Datenschutzfreundliche Alternative
3. **GitHub Insights:** Repository → Insights → Traffic

---

## ✅ Checklist

- [ ] Git Repository initialisiert
- [ ] Dateien committed und gepusht
- [ ] GitHub Pages aktiviert (Settings → Pages)
- [ ] 2 Minuten gewartet
- [ ] Seite funktioniert unter https://entaroadunexecutar.github.io/Lechbruck-guide/
- [ ] Auf Handy getestet
- [ ] Als PWA installiert (optional)
- [ ] Mit Freunden/Familie geteilt 🎉

---

**Viel Erfolg beim Deployment! 🚀**

Bei Fragen: Öffne ein Issue im Repository!

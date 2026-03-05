# Deploy su GitHub e link pubblico

## 1. Crea il repository su GitHub

1. Vai su [github.com/new](https://github.com/new).
2. Nome repository: **abbigliamento** (così l’URL sarà `https://salvo934.github.io/abbigliamento/`).
3. Scegli **Public**, non aggiungere README (il progetto ce l’hai già in locale).
4. Clicca **Create repository**.

## 2. Collega il progetto e fai il primo push

Se non hai ancora inizializzato git nella cartella del progetto:

```bash
cd "/Users/salvatorebonavita/Desktop/ABBIGLIAMENTO "
git init
git add .
git commit -m "Deploy su GitHub Pages"
git branch -M main
git remote add origin https://github.com/salvo934/abbigliamento.git
git push -u origin main
```

Se il repo esiste già ma non hai ancora pushato:

```bash
git add .
git commit -m "Deploy su GitHub Pages"
git push -u origin main
```

## 3. Attiva GitHub Pages

1. Sul repository **abbigliamento** su GitHub: **Settings** → **Pages**.
2. In **Build and deployment** → **Source** scegli **GitHub Actions**.
3. Salva (non serve creare un workflow a mano: è già presente `.github/workflows/deploy-pages.yml`).

## 4. Aspetta il deploy

- Dopo il push, vai in **Actions** nel repo: partirà il workflow **Deploy su GitHub Pages**.
- Attendi che finisca (circa 1–2 minuti).
- Il link del sito sarà:

  **https://salvo934.github.io/abbigliamento/**

Da quel momento ogni `git push` su `main` farà partire di nuovo il deploy e aggiornerà il sito.

---

**Prova da altri dispositivi:** apri il link sopra da smartphone o da un altro PC; non serve essere loggati su GitHub.

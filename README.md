# Site personnel — portfolio & blog

## Présentation

Ce dépôt héberge mon site web personnel. Le site sert de vitrine : présentation du parcours, mise en avant de projets data, articles de blog (retours d’expérience, notes techniques) et de point de contact pour les opportunités professionnelles.

Le site est pensé comme un espace simple à maintenir, lisible, et professionnel.

## Description du projet

Le site est structuré autour de plusieurs pages principales :

| Page | Rôle |
|------|------|
| **Accueil** | Introduction, expertise et liens vers les sections clés |
| **À propos** | Parcours, formation, expériences et compétences |
| **Projets** | Portfolio de réalisations (liens vers dépôts ou ressources externes) |
| **Blog** | Liste des articles publiés dans `_posts/` (Markdown) |
| **Contact** | Coordonnées, CV et prise de rendez-vous |

Le déploiement est assuré par **GitHub Pages** : le dépôt `ksondeji.github.io` est le site utilisateur GitHub, ce qui permet une mise en ligne automatique à partir de la branche `main`.

## Stack technique

| Élément | Choix |
|---------|--------|
| Générateur | [Jekyll](https://jekyllrb.com/) | De nombreuses fonctionalités natives pour plus de simplicité
| Thème | [Minima](https://github.com/jekyll/minima) (thème par défaut Jekyll, personnalisable) |
| Hébergement | [GitHub Pages](https://pages.github.com/) |
| Contenu | Pages et articles en **Markdown** ; mises en page personnalisées dans `_layouts/` |
| Styles | SCSS dans `assets/` (ex. `assets/main.scss`) |
| Plugins Jekyll | `jekyll-feed` (flux RSS), `jekyll-sitemap` (plan du site), `jekyll-seo-tag` (balises SEO) |
| Analytics | Google Analytics (identifiant configuré dans `_config.yml`) |


## Installation locale & accès rapide

### Consulter le site en ligne

Ouvrir : **https://ksondeji.github.io**

### Prérequis (développement local)

- [Ruby](https://www.ruby-lang.org/) (version compatible avec Jekyll, selon votre OS)
- [Bundler](https://bundler.io/) (recommandé si vous ajoutez un `Gemfile`)

> **Note :** ce dépôt ne contient pas forcément de `Gemfile` : GitHub Pages résout les versions des gems côté serveur. Pour un environnement local reproductible, vous pouvez ajouter un `Gemfile` aligné avec [la doc GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll).

### Lancer le site en local (sans Gemfile)

Depuis la racine du dépôt :

```bash
gem install bundler jekyll
jekyll serve
```

Puis ouvrir **http://127.0.0.1:4000** (ou l’URL indiquée dans le terminal).

### Lancer avec Bundler (si vous ajoutez un Gemfile)

```bash
bundle install
bundle exec jekyll serve
```

Les fichiers modifiés sont recompilés automatiquement en général ; un rechargement du navigateur suffit pour voir les changements.

## Contact

Les canaux à jour sont listés sur la page **Contact** du site : **https://ksondeji.github.io/contact/**

À titre indicatif (vérifier sur le site en cas de mise à jour) :

- **E-mail :** [karl.sondeji@gmail.com](mailto:karl.sondeji@gmail.com)
- **LinkedIn :** profil lié depuis la page Contact
- **GitHub :** [@ksondeji](https://github.com/ksondeji)

Pour une collaboration ou un échange, la page Contact propose aussi un lien vers Calendly et le téléchargement du CV.

## Prochaines étapes du projet

Pistes naturelles d’évolution (à prioriser selon vos objectifs) :

1. **Blog** — Publier les premiers billets dans `_posts/` pour activer la liste sur `/blog/` et le flux RSS (`jekyll-feed`).
2. **Cohérence SEO & réseaux** — Finaliser les champs optionnels dans `_config.yml` (ex. pseudo Twitter/X si utilisé) pour que `jekyll-seo-tag` reflète exactement votre présence.
3. **Thème & identité** — Affiner couleurs, typographie et composants Minima via `assets/main.scss` et surcharges dans `_layouts/` / `_includes/` pour renforcer la charte personnelle.
4. **Qualité de build** — Ajouter un `Gemfile` + `Gemfile.lock` pour figer les versions en local et faciliter les contributions ou la CI.
5. **Contenu portfolio** — Tenir `projets.md` à jour et ajouter captures ou résumés courts pour chaque réalisation mise en avant.

---

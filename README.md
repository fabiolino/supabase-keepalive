# supabase-keepalive

Visite quotidienne des projets Supabase gratuits (Respire, Italia Autentica) pour éviter leur mise en pause.

Supabase met en pause un projet gratuit après **7 jours sans activité**. Ce dépôt lance chaque jour,
sur GitHub Actions, une petite lecture dans chaque projet listé : cela compte comme une activité.

## Projets visités

| Projet | Tableau de bord |
|---|---|
| Respire Network | https://supabase.com/dashboard/project/nnjtndclcoooawrisgmf |
| Italia Autentica | https://supabase.com/dashboard/project/pttrvqsiqrncjaokpylz |

Spritz Connection n'en a pas besoin : il est dans l'organisation Pro, qui ne se met jamais en pause.

## Vérifier que ça tourne

Onglet **Actions** du dépôt : https://github.com/fabiolino/supabase-keepalive/actions
Une coche verte par jour = tout va bien. En cas d'échec, GitHub envoie un e-mail, et le détail
de la visite indique le lien pour relancer le projet concerné.

## Ajouter un projet (par exemple Moments)

Dans `.github/workflows/keepalive.yml`, ajouter un bloc dans `matrix.include` avec le nom, la référence
du projet, sa clé « publishable » et le nom d'une table existante.

## Limites

- Pas de sauvegarde automatique quotidienne sur le plan gratuit : pour un projet dont les données
  deviennent importantes, passer au plan Pro.
- Si Supabase change ses règles de mise en pause, cette visite peut ne plus suffire : surveiller les e-mails d'échec.

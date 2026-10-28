# DashLord

Tableau de bord des bonnes pratiques techniques : https://dashlord.mte.incubateur.net

## Usage

### Ajouter une URL dans le dashlord

Vous devez éditer le fichier [./dashlord.yml](./dashlord.yml) et ajouter une entrée pour votre URL.

💡 Bonne pratique : enlever les slashs à la fin des urls

Exemple d'entrée pour une URL :

```yml
- url: https://www.free.fr
  title: Homepage free.fr
  betaId: free # optionnel, id de la startup sur beta.gouv.fr
  tags: # optionnel
    - telecom
    - provider
  repositories: # optionnel, pour récupérer les alertes de sécu de ces repos
    - free/free-ui
    - free/free-css
  tools: # optionnel, pour desactiver certains outils
    nmap: false
  pages: # optionnel, pour lancer lighthouse sur des pages supplémentaires
    - /profil
    - /mentions
```

Pour la documentation de DashLord lui-même : https://github.com/SocialGouv/dashlord


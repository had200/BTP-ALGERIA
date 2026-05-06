# BTP Algeria — Système de Gestion Intégré

Plateforme web de gestion destinée aux entreprises du bâtiment et des travaux publics (BTP) en Algérie. Le système centralise les opérations administratives, financières, humaines et opérationnelles, avec une attention particulière portée à la sécurité des données.

## Fonctionnalités principales

- **Comptes et authentification** : gestion des utilisateurs, contrôle d'accès basé sur les rôles (RBAC) et authentification à deux facteurs.
- **Gestion des employés** : dossiers du personnel, paie et congés.
- **Gestion des projets** : suivi des chantiers, situations de travaux et rentabilité.
- **Gestion des fournisseurs** : achats, devis, stocks et facturation.
- **Gestion financière** : comptabilité selon le Système Comptable Financier (SCF), trésorerie et suivi fiscal.
- **Gestion du parc automobile** : suivi des engins, maintenance et carburant.
- **Audit** : journalisation des opérations sensibles.

## Technologies

- Python et Django
- PostgreSQL
- Redis
- Docker et Docker Compose
- HTML, CSS et JavaScript

## Installation locale

### 1. Cloner le dépôt

```bash
git clone https://github.com/had200/BTP-ALGERIA.git
cd BTP-ALGERIA
```

### 2. Créer un environnement virtuel

```bash
python -m venv venv
```

Sous Windows :

```powershell
venv\Scripts\activate
```

Sous Linux ou macOS :

```bash
source venv/bin/activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 4. Configurer les variables d'environnement

Copier le fichier `.env.example` vers `.env`, puis renseigner les paramètres nécessaires à l'environnement local.

Ne jamais publier le fichier `.env` ni y inscrire des identifiants réels dans le dépôt.

### 5. Démarrer les services

Si Docker et Docker Compose sont configurés :

```bash
docker compose up -d
```

### 6. Appliquer les migrations

```bash
python manage.py migrate
```

### 7. Lancer le serveur Django

```bash
python manage.py runserver
```

L'application sera accessible à l'adresse :

http://127.0.0.1:8000/

## Structure des modules

| Module | Description |
|---|---|
| `accounts` | Authentification et gestion des accès |
| `employees` | Gestion des employés |
| `projects` | Suivi des projets et chantiers |
| `suppliers` | Gestion des fournisseurs et achats |
| `finance` | Gestion financière et comptable |
| `fleet` | Gestion du parc automobile |
| `audit` | Journalisation des opérations sensibles |
| `dashboard` | Tableau de bord |

## Sécurité

Le projet intègre plusieurs mécanismes de sécurité, notamment la gestion des rôles, la protection des accès, le chiffrement de données et la journalisation des actions sensibles.

Pour plus d'informations, consulter le fichier `SECURITY_CHECKLIST.md`.

## Démonstration

Les comptes de démonstration et leurs identifiants doivent être configurés localement. Aucun mot de passe réel ou identifiant sensible n'est fourni dans ce dépôt.

## Licence

À définir.

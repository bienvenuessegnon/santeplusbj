# Santé+ Bénin

Plateforme d'accès aux soins au Bénin : patients, professionnels de santé et établissements, avec carte, rendez-vous, documents médicaux et paiements en FCFA ou en Bitcoin Lightning.

*A health-access platform for Benin (patients, practitioners and facilities), with a map, appointments and Lightning payments. Built for the Bitcoin Mastermind Hackathon 2026 (2nd place, team Winners).*

**Démo :** [https://santepluspro.onrender.com/](https://santepluspro.onrender.com/)

## Fonctionnalités

Espace patient :

- création de compte et profil
- recherche d'établissements et carte interactive
- prise de rendez-vous et consultation des tarifs
- dossier et documents médicaux (ordonnances, analyses, devis)
- portefeuille en FCFA et paiement via le Lightning Network
- factures et reçus

Espace établissement / médecin :

- tableau de bord des rendez-vous et des patients
- ordonnances et documents
- demandes d'accès aux dossiers (identifiant patient)

Les intégrations d'assistance (clé `GEMINI_API_KEY`, optionnelle) complètent l'interface ; elles ne remplacent pas un avis médical. L'intégrité de certains documents est contrôlée par un hachage SHA-256.

## Stack

- Interface : React, TypeScript, Vite, Tailwind CSS, Leaflet
- API : FastAPI (Python)
- Paiements : portefeuille FCFA et Bitcoin Lightning

## Lancer le projet

Prérequis : Node.js et Python 3.9+.

Interface (port 3000 par défaut) :

```bash
cp .env.example .env
npm install
npm run dev
```

API :

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

Documentation interactive de l'API : [http://localhost:8000/docs](http://localhost:8000/docs).

## Structure

```text
src/          interface React
backend/      API FastAPI (hôpitaux, rendez-vous, portefeuille, documents)
server.ts     serveur de développement de l'interface
FEATURES.md   détail fonctionnel
```

## Équipe

Projet réalisé par l'équipe **Winners** au **Bitcoin Mastermind Hackathon 2026** (2e place) : Bienvenu ESSEGNON, Adorée KPENONHOUN, Orphet AHILIHAN, Ismail AGOHOUNDJE et Prince BONGO.

## Auteur

[Bienvenu ESSEGNON](https://github.com/bienvenuessegnon) · [bienvenuessegnon01@gmail.com](mailto:bienvenuessegnon01@gmail.com)

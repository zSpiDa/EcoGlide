# 🚲 EcoGlide

[🇬🇧 English version](README.md)

**Piattaforma di Smart Mobility sviluppata con Django e Django REST Framework**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-Web%20Framework-green?logo=django&logoColor=white)
![Django REST Framework](https://img.shields.io/badge/DRF-REST%20API-red)
![JWT](https://img.shields.io/badge/Auth-JWT-orange)

## Panoramica del progetto

EcoGlide è un progetto accademico di Ingegneria del Software incentrato sulla progettazione e implementazione di una piattaforma per la gestione della mobilità intelligente e del vehicle sharing.

Il sistema fornisce un backend sviluppato con Django e API REST per la gestione di utenti, veicoli condivisi, corse, aree urbane, segnalazioni di manutenzione e diversi servizi legati alla mobilità.

Il progetto include inoltre dashboard frontend dedicate a differenti tipologie di utenti e una serie di servizi esterni simulati utilizzati per rappresentare funzionalità di routing, meteo e pagamento.

## Funzionalità principali

- Gestione utenti e ruoli
- Autenticazione basata su JWT
- Gestione dei veicoli condivisi
- Creazione e gestione del ciclo di vita delle corse
- Gestione di aree urbane e zone con restrizioni
- Segnalazioni di manutenzione dei veicoli
- Dashboard per operatori e Pubblica Amministrazione
- Analisi sull'utilizzo del servizio
- Statistiche sul risparmio di CO₂
- Statistiche su ricavi e corse
- Servizio di routing simulato
- Informazioni meteo simulate
- Sistema di pagamento mock

## Tecnologie utilizzate

- Python
- Django
- Django REST Framework
- Simple JWT
- SQLite
- HTML
- CSS
- JavaScript

## Architettura

Il progetto è organizzato intorno a un backend Django e a un frontend leggero.

```text
EcoGlide/
├── config/
│   ├── settings.py
│   └── urls.py
├── mobility/
│   ├── models.py
│   ├── serializers.py
│   ├── services.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── frontend_app/
│   ├── index.html
│   ├── dashboard_operatore.html
│   └── dashboard_pa.html
├── manage.py
├── requirements.txt
├── README.md
├── README.it.md
└── .gitignore
```

## Servizi simulati

Alcune integrazioni sono intenzionalmente implementate come simulazioni o mock per finalità accademiche.

### Routing

Il componente di routing genera percorsi tenendo conto delle aree urbane soggette a restrizioni.

Non utilizza un provider di routing esterno e deve quindi essere considerato un servizio di routing simulato, non un sistema di navigazione destinato all'utilizzo in produzione.

### Meteo

Le informazioni meteorologiche vengono generate localmente a scopo dimostrativo e non utilizzano API meteo reali.

### Pagamenti

Le operazioni di pagamento vengono simulate tramite un gateway mock e non elaborano transazioni finanziarie reali.

Questi componenti sono stati progettati in modo da poter essere sostituiti con provider esterni reali in una possibile implementazione orientata alla produzione.

## Installazione

Clona il repository:

```bash
git clone https://github.com/zSpiDa/EcoGlide.git
cd EcoGlide
```

Crea un ambiente virtuale.

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Installa le dipendenze:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Applica le migrazioni del database:

```bash
python manage.py migrate
```

Facoltativamente, popola il database con dati di esempio:

```bash
python manage.py seed_db
```

Avvia il server backend:

```bash
python manage.py runserver
```

L'API sarà disponibile all'indirizzo:

```text
http://127.0.0.1:8000/
```

I file frontend possono essere aperti dalla directory `frontend_app/`.

Assicurati che il base URL delle API utilizzato dal frontend punti a:

```text
http://127.0.0.1:8000/api
```

## Esecuzione dei test

Per eseguire la suite di test Django:

```bash
python manage.py test
```

## Contesto accademico

EcoGlide è stato sviluppato come progetto accademico per il corso di **Ingegneria del Software**.

Il progetto è incentrato su architettura software, progettazione di API REST, modellazione del dominio e implementazione di un workflow per la gestione della mobilità tramite Django.

## Disclaimer

I servizi di routing, meteo e pagamento sono simulati per finalità didattiche e non sono destinati all'utilizzo in produzione.

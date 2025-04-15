# Lavoro-di-gruppo-15-04
Esercitazione 
# 🎭 Gestione Teatro

Un sistema in Python per gestire la prenotazione dei posti in un teatro, con supporto a posti VIP e Standard. Il progetto include un menù interattivo da terminale per facilitare l'interazione con l'utente.

## 📦 Funzionalità

- Aggiunta di posti **Standard** (con costo) e **VIP** (con servizi extra)
- Prenotazione e liberazione dei posti
- Visualizzazione dei posti disponibili e di quelli occupati
- Sistema a oggetti basato su classi ereditate (`Posto`, `PostoVIP`, `PostoStandard`)
- Menù interattivo testuale

## 🧱 Struttura delle classi

### `Posto` (classe base)
- Attributi:
  - `numero` (int)
  - `fila` (str)
  - `occupato` (bool)
- Metodi:
  - `prenota()`
  - `libera()`
  - `get_numero()`, `get_fila()`, `is_occupato()`

### `PostoStandard` (sottoclasse)
- Attributi aggiuntivi:
  - `costo` (float)
- Sovrascrive `prenota()` per mostrare il costo

### `PostoVIP` (sottoclasse)
- Attributi aggiuntivi:
  - `servizi_extra` (list)
- Sovrascrive `prenota()` per attivare i servizi extra

### `Teatro`
- Contiene una lista di posti (VIP e Standard)
- Metodi:
  - `aggiungi_posto(posto)`
  - `prenota_posto(numero, fila)`
  - `libera_posto(numero, fila)`
  - `stampa_tutti_posti()`
  - `stampa_posti_occupati()`

## 🚀 Come avviare il progetto

1. Assicurati di avere Python installato (versione 3.7 o superiore).
2. Esegui lo script da terminale:

```bash
python nome_script.py

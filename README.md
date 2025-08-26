# GlobalSearch Plugin

Un plugin Spigot per Minecraft 1.16.5+ che permette la ricerca globale di items identici in tutto il server.

## Caratteristiche

### 🔍 Ricerca Avanzata
- Ricerca items identici in **tutti** gli inventari e container del server
- Confronto completo: materiale, nome, lore, NBT tags, custom model data, durabilità
- Ricerca in inventari di player online e offline
- Ricerca in tutti i tipi di container (bauli, barili, fornaci, etc.)

### 🎮 Comandi
- `/globalsearch hand` - Cerca l'item in mano ovunque
- `/globalsearch offline` - Cerca solo negli inventari dei player offline  
- `/globalsearch player` - Cerca solo negli inventari dei player
- `/globalsearch container` - Cerca solo nei container del mondo
- `/globalsearch`, `/wgs`, `/gs`, `/gsearch` - Alias comandi

### 🖥️ GUI Interattiva
- **Interfaccia intuitiva** con icone rappresentative
- **Container**: Icona del tipo di container + coordinate per il teleport
- **Player**: Testa del player + status online/offline
- **Navigazione** con pagine dei risultati
- **Click Actions**: Teleport ai container o apertura inventari player

### ⚡ Performance
- **Ricerca asincrona** per evitare lag al server
- **Timeout configurabile** per ricerche ampie
- **Ottimizzazioni** per server con molti dati

### 🔐 Permessi
- `globalsearch.admin` - Accesso completo a tutte le funzionalità del plugin

## Installazione

1. **Scarica** il file JAR del plugin
2. **Scarica** le dipendenze del plugin
3. **Posiziona** il file nella cartella `plugins/` del tuo server
4. **Riavvia** il server

## Dipendenze

### Richieste
- **Spigot/Paper** 1.16.5 o superiore
- **Java** 8 o superiore
- **NBT-API**
- **OpenInv**

## Configurazione

```yaml
settings:
  max-results: 500              # Massimo numero di risultati
  search-timeout-seconds: 30    # Timeout ricerca in secondi
  async-search: true           # Ricerca asincrona
  search-loaded-chunks-only: false # Solo chunk caricati (più veloce)
```

## Come Usare

1. **Tieni l'item** che vuoi cercare nella mano principale
2. **Esegui il comando** appropriato:
   - `/globalsearch hand` per ricerca completa
   - `/globalsearch container` per solo container
   - `/globalsearch player` per solo inventari player
3. **Naviga** i risultati nella GUI:
   - **Click su container** → Teleport alla posizione
   - **Click su player** → Apre inventario con `/oi <player>`

## Esempi d'Uso

### Ricerca globale
```
/globalsearch hand
```
Cerca l'item che hai il mano globalmente

### Filtra solo nei bauli
```
/globalsearch container  
```
Cerca solo nei container del mondo (bauli, barili, etc.)

### Filtra solo inventari offline
```
/globalsearch offline
```
Cerca solo negli inventari dei player che non sono online

## Funzionalità Tecniche

### Ricerca Items
Il plugin utilizza **NBT-API**:
- ✅ **Tutti i tag NBT** (completo al 100%)
- ✅ Tipo di materiale
- ✅ Nome personalizzato  
- ✅ Lore completo
- ✅ Enchantments
- ✅ Custom Model Data
- ✅ Durabilità
- ✅ Attributi e modificatori
- ✅ Flag items
- ✅ Stato unbreakable
- ✅ **Dati plugin personalizzati** (QualityArmory, ItemsAdder, etc.)
- ✅ **Tag nascosti e custom data**
- ✅ **Metadati avanzati**

### Tipi di Container Supportati
- Bauli normali e intrappolati
- Barili
- Shulker Box
- Tramogge
- Fornaci e varianti
- Dropper e Dispenser
- E molti altri...

## Supporto

Per bug, suggerimenti o richieste di funzionalità, contattami su Telegram: @alez1337

## Licenza

Questo plugin è sviluppato per uso privato. Tutti i diritti riservati.

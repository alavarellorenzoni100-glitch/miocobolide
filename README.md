# Guida al mio nuovoidecobol

# 🚀 Guida Rapida: nuovoidecobol

Questa guida ti aiuterà a configurare e utilizzare l'ambiente di sviluppo integrato (IDE) a menu per COBOL, disponibile in diverse implementazioni (C, Python e Node.js).

## 🛠️ Requisiti di Sistema

Prima di iniziare, assicurati di avere installato i seguenti componenti:

* **GnuCOBOL (`cobc`)**: Deve essere installato e presente nel PATH del sistema.
* **Compilatore C (`gcc`)**: Necessario per compilare la versione principale dell'IDE.
* **Editor di testo**: `vim` o `nano` (l'IDE si appoggia a questi per la modifica dei file).
* **Ambienti opzionali**: `python3` o `node` se desideri utilizzare le versioni alternative dell'IDE.

---

## ⚙️ Installazione e Configurazione

Puoi scegliere di compilare la versione nativa in C o utilizzare gli interpreti per Python/Node.js.

### 1. Versione C (Consigliata)

Per generare l'eseguibile principale `cobol_ide_c`, esegui:

```bash
gcc -o cobol_ide_c cobol_ide.c

```

### 2. Versioni Alternative

* **Python**: `python3 cobol_ide.py`
* **Node.js**: `node cobol_ide.js`

---

## 🖥️ Come utilizzare l'IDE

### Avvio

Il modo più semplice per iniziare è utilizzare lo script di avvio predefinito, che cercherà ed eseguirà automaticamente il binario C:

```bash
./start-ide-cobol.sh

```

### Comandi del Menu

Una volta avviato, l'IDE presenta quattro opzioni principali:

1. **Create/Edit COBOL file**: Apre l'editor per creare o modificare file con estensione `.cob`.
2. **Compile COBOL file**: Avvia la compilazione tramite `cobc`.
3. **Run compiled program**: Esegue il programma COBOL appena compilato.
4. **Exit**: Chiude l'applicazione.

---

## 📝 Esempio: Il tuo primo "Hello World"

Segui questi passaggi per testare l'installazione:

1. Seleziona l'opzione **1** nel menu e crea un file chiamato `hello.cob`.
2. Inserisci il seguente codice:
```cobol
       IDENTIFICATION DIVISION.
       PROGRAM-ID. HELLO.
       PROCEDURE DIVISION.
           DISPLAY "Hello, World!".
           STOP RUN.

```


3. Seleziona l'opzione **2** per compilare (oppure usa manualmente `cobc -x -o hello hello.cob`).
4. Seleziona l'opzione **3** per eseguire il programma (oppure usa `./hello` da terminale).

---

## 📁 Struttura del Repository

* `cobol_ide.c/py/js`: Implementazioni dell'IDE in vari linguaggi.
* `start-ide-cobol.sh`: Script di avvio rapido.
* `COBOL_TUTORIAL.md`: Tutorial dettagliato sul linguaggio COBOL.

> **Nota:** Il progetto è rilasciato sotto licenza **Apache License 2.0**.


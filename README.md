📘 Na klar, Alex! Hier sind zwei passende **README-Beschreibungen** für deine Skripte `rocm_rdna2_auto.run` und `KI_test.run`, die du direkt in dein GitHub-Repository oder als Dokumentation verwenden kannst:

---

## 📦 `rocm_rdna2_auto.run` – Automatisches ROCm-Setup für RDNA2-Systeme

### 🔧 Zweck  
Dieses Skript automatisiert die Installation der passenden ROCm-Version auf Ubuntu-Systemen mit RDNA2-Grafikhardware. Es erkennt Kernel- und OS-Versionen und passt die Setup-Schritte dynamisch an.

### 🚀 Features  
- Automatische Erkennung von Kernel + Ubuntu-Version  
- Auswahl der geeigneten ROCm-Version (`5.7`, `6.0`, `6.1`)  
- Entfernt alte Treiber-Installationen  
- Fügt neues Repository hinzu & lädt GPG-Schlüssel  
- Installiert `rocm-dev`, `hipcc`, `clinfo`, `rocminfo`, `dkms`  
- Setzt alle nötigen Umgebungsvariablen inklusive `HSA_OVERRIDE_GFX_VERSION`  
- Validiert die Installation durch `clinfo` und `rocminfo`

### ▶️ Ausführung  
```bash
wget https://raw.githubusercontent.com/Karli000/AMD-Rocm/main/rocm_rdna2_auto.run
chmod +x rocm_rdna2_auto.run
./rocm_rdna2_auto.run
```

### 📁 Logdatei  
Ergebnisse werden in `rocm_setup.log` gespeichert

---

## 🧪 `KI_test.run` – Komponententest für ROCm Setup

### 🔧 Zweck  
Dieses Skript überprüft, ob alle relevanten Komponenten für KI-Workloads korrekt installiert und ausführbar sind. Es setzt eine eigene Python-Umgebung (venv) auf und führt CLI-Tests durch.

### 🚀 Features  
- Erstellt venv und installiert: `notebook`, `tensorflow`, `matplotlib`, `pandas`  
- Testet Verfügbarkeit von:
  - `hipcc` (HIP-Compiler)
  - `jupyter` (CLI-basiert mit Diagnosetext)
  - `blender`
  - `tensorflow` (Importprüfung)
- Gibt eine Status-Tabelle direkt im Terminal aus  
- Speichert alle Ergebnisse in `KI_test.log`

### ▶️ Ausführung  
```bash
wget https://raw.githubusercontent.com/Karli000/AMD-Rocm/main/KI_test.run
chmod +x KI_test.run
./KI_test.run
```

### 📁 Logdatei  
Protokolliert den Testverlauf und die Ergebnisse in `KI_test.log`

---

✅ Du kannst diese Beschreibungen auch in deinem Repository als `README.md` ergänzen oder direkt im GitHub-Editor nutzen. Willst du, dass ich sie als Markdown-Datei formatiere, die du direkt einfügen kannst? 😄📘

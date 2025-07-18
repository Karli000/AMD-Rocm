## 📦 `rocm_rdna2_auto.run` – ROCm 6.4.1 Setup für RDNA2-Systeme Ubuntu 22.04.-24.04. Kernel 5.15-6.14 erkennt System automatisch

### 🔧 Zweck  
Dieses Skript installiert **ausschließlich ROCm 6.4.1** auf Ubuntu-Systemen mit RDNA2-Grafikhardware.

### 🚀 Funktionen  
- Entfernt alte ROCm-Installationen und Treiber  
- Fügt das ROCm 6.4.1-Repository hinzu und lädt GPG-Schlüssel  
- Installiert: `rocm-dev`, `hipcc`, `clinfo`, `rocminfo`  
- Setzt alle nötigen Umgebungsvariablen:
  - `ROCM_PATH`, `LD_LIBRARY_PATH`, `PATH`
  - `HSA_OVERRIDE_GFX_VERSION` (für RDNA2 z. B. gfx1030)
- Führt `clinfo` und `rocminfo` zur Validierung aus

### ▶️ Ausführung

```bash
wget https://raw.githubusercontent.com/Karli000/AMD-Rocm/main/rocm_rdna2_auto.run
chmod +x rocm_rdna2_auto.run
./rocm_rdna2_auto.run
```

### 📁 Logdatei  
Alle Installationsschritte werden in `rocm_setup.log` protokolliert.

---

## 🧪 `KI_test.run` – Komponententest für ROCm 6.4.1 Umgebung

### 🔧 Zweck  
Testet zentrale Tools für KI-Workloads nach der Installation von ROCm 6.4.1.

### 🚀 Funktionen  
- Erstellt eigene Python-Umgebung (`venv`)  
- Installiert:  
  - `notebook`, `tensorflow`, `matplotlib`, `pandas`  
- Prüft Verfügbarkeit von:
  - `hipcc` (HIP Compiler)
  - `jupyter` (CLI-Test via `--version`)
  - `blender`
  - `tensorflow` (Importprüfung)
- Gibt übersichtliche Status-Tabelle im Terminal aus  
- Logdatei: `KI_test.log`

### ▶️ Ausführung

```bash
wget https://raw.githubusercontent.com/Karli000/AMD-Rocm/main/KI_test.run -O KI_test.run
chmod +x KI_test.run
./KI_test.run
```

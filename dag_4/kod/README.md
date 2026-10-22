# Kod dag 4

Dag 4 innehåller hela Pythonflödet så att studenten kan återskapa analys och modell inför redovisningen.

CSV-filen ingår inte i studentpaketet utan hämtas från UCI med det medföljande skriptet.

## Linux/macOS

Skapa den virtuella miljön och installera beroendena första gången:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r dag_4/kod/python/requirements.txt
```

Om miljön redan finns behöver den bara aktiveras:

```bash
source .venv/bin/activate
```

## Windows PowerShell

Skapa den virtuella miljön och installera beroendena första gången:

```powershell
python -m venv .venv
```

Om PowerShell blockerar aktiveringsskriptet kan körning tillåtas tillfälligt i det aktuella PowerShell-fönstret:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```

Inställningen upphör när PowerShell-fönstret stängs. Den som i stället vill ändra inställningen för sin användare kan köra:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Aktivera miljön och installera beroendena:

```powershell
.\.venv\Scripts\activate.ps1
python -m pip install -r dag_4/kod/python/requirements.txt
```

När miljön redan finns räcker det normalt att aktivera den:

```powershell
.\.venv\Scripts\activate.ps1
```

## Kör analysen på båda operativsystemen

Kör från kursens rotmapp efter att miljön har aktiverats:

```text
python dag_4/kod/python/download_data.py
python dag_4/kod/python/analyze_iot.py dag_4/kod/data/ai4i2020.csv
python dag_4/kod/python/train_model.py dag_4/kod/output/ai4i_clean.csv
```

Resultaten sparas i `dag_4/kod/output/`.

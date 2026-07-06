# Coding Challenge IDS

Prototyping-Lösungen für einen Stahlhersteller mit Laufrobotern (Quadrupeds).
Das Repo enthält **zwei Teilprojekte**, die unabhängig voneinander bearbeitet werden.

| Teilprojekt | Thema | Ordner | Lead |
|---|---|---|---|
| **TP01** | Routenoptimierung – maximale Abdeckung der QA-Runden durch drei Roboter | [`tp01_routenoptimierung/`](tp01_routenoptimierung/) | Lilli |
| **TP03** | Roboterkinematik – direkte & inverse Kinematik für einen 2-Gelenk-Arm | [`tp03_kinematik/`](tp03_kinematik/) | Sophia |

Die genauen Aufgabenstellungen stehen in der jeweiligen `README_EN.ipynb` im Teilprojekt-Ordner. **Diese Aufgaben-READMEs bitte nicht verändern** – sie sind unsere Referenz.

---

## Ordnerstruktur

```
Coding-Challenge-IDS/
├── README.md                    ← diese Datei
├── .gitignore
├── tp01_routenoptimierung/
│   ├── README_EN.ipynb          ← Aufgabenstellung (nicht ändern)
│   ├── submission_tp01_optimization.ipynb   ← unsere Abgabe
│   └── data/                    ← points_*.txt, ls_matrix_*.txt
└── tp03_kinematik/
    ├── README_EN.ipynb          ← Aufgabenstellung (nicht ändern)
    ├── abgabe_tp3_direkte_kinematik.ipynb   ← unsere Abgabe
    ├── abgabe_tp3_inverse_kinematik.ipynb   ← unsere Abgabe
    └── 2_link_robot.png
```

---

## Team & Zuständigkeiten

| Person | Branch | Zuständig für |
|---|---|---|
| Lilli | `lilli` (+ verwaltet `main`) | TP01 Lead: Kernalgorithmik (Nearest-Neighbor + 5-h-Check, Roboter-Aufteilung, Trade-off) |
| Anna | `anna` | TP01: Reader-Funktionen + Scatterplot |
| Lea | `lea` | TP01: Einzelrundwege der Restmaschinen + Laufzeitkomplexität |
| Sophia | `sophia` | TP03 Lead: direkte Kinematik + Visualisierung |
| Aylin | `aylin` | TP03: inverse Kinematik |

---

## Git-Workflow

**Wichtigste Regel: Niemand pusht direkt auf `main`.** `main` ist geschützt – nur Lilli merged zentral über Pull Requests.

Jede arbeitet ausschließlich auf ihrem eigenen Branch.

### Einmalig: Repo klonen und auf den eigenen Branch wechseln

```bash
git clone https://github.com/lilikts/Coding-Challenge-IDS.git
cd Coding-Challenge-IDS
git fetch origin
git switch anna          # euren eigenen Branch-Namen einsetzen
```

### Täglich: arbeiten, committen, pushen

```bash
git add .
git commit -m "kurze, klare Beschreibung"
git push origin anna     # euren eigenen Branch
```

### Wenn eure Arbeit nach `main` soll

1. Auf GitHub einen **Pull Request** von eurem Branch → `main` öffnen.
2. Lilli prüft und merged.

### Aktuellen Stand von `main` in euren Branch holen

Damit ihr nicht auf einem veralteten Stand arbeitet:

```bash
git switch anna
git fetch origin
git merge origin/main
```

---

## Setup / Umgebung

- **Python** über Anaconda (Python 3.13)
- **VS Code** mit den Extensions *Python* und *Jupyter*
- Notebooks (`.ipynb`) werden direkt in VS Code geöffnet und ausgeführt – kein separates JupyterLab nötig
- Als Kernel das Anaconda-Environment auswählen

Alle Dateipfade in den Notebooks sind **relativ** (z. B. `data/ls_matrix_55_42.txt`), damit es bei allen gleich läuft.

---

## Notebook-Hygiene (wichtig gegen Merge-Konflikte)

`.ipynb`-Dateien sind intern JSON und neigen zu hässlichen Merge-Konflikten. Deshalb:

- Möglichst **nicht zu zweit gleichzeitig** im selben Notebook arbeiten (durch die Themen-Aufteilung ohnehin selten).
- **Vor dem Commit** die Outputs leeren: *Kernel → Restart & Clear Output*. Das hält die Diffs klein.

---

## Termine

- **10.07.** – Draft-Präsentation
- **31.07. 23:59** – Endpräsentation + Upload (in **ILIAS**, nicht über GitHub!)

> Denkt dran: Die Abgabe läuft über den ILIAS-Upload. Stellt sicher, dass die finalen Notebooks rechtzeitig dort landen und nicht nur im Repo liegen.

# How to run the notebooks

You need **one** of the three options below. All notebooks run top to bottom: click a cell and press
`Shift + Enter`, or use *Run all*. You cannot break anything - if something goes wrong, restart and run all again.

> **Internet is required in all options**: the first cell that loads data downloads a small public CSV file
> (about 1 MB) from the Hugging Face website.

---

## Option 1 - Google Colab (recommended, nothing to install)

Needs a free **Google account** and a browser (laptop, tablet or phone with a large screen).

**Fastest way**
1. Open this repository on GitHub and click the **Open in Colab** badge of the notebook you want (see [README](README.md)).
2. Sign in with your Google account if asked.
3. If Colab shows *"Notebook not authored by Google"*, click **Run anyway**.
4. Menu **Runtime → Run all** (or run cell by cell with `Shift + Enter`).

**Alternative (if the badge does not open)**
1. Go to <https://colab.research.google.com>.
2. **File → Open notebook → GitHub** tab.
3. Paste `simonkng/ophthalmology-ml-workshop` and press Enter, then choose the notebook.

**Alternative: upload the file**
1. Download the `.ipynb` file from GitHub (open it, click the download icon, or use *Raw → Save as*).
2. In Colab: **File → Upload notebook** and choose the file.

Tips
- Colab sessions end after a period of inactivity; your changes are lost unless you use *File → Save a copy in Drive*.
- All required libraries (pandas, scikit-learn, matplotlib, seaborn) are already installed in Colab.

---

## Option 2 - Kaggle Notebooks

Needs a free **Kaggle account** (<https://www.kaggle.com>).

1. Sign in to Kaggle. Switching on the internet inside notebooks requires a **phone-verified** account
   (Kaggle → your profile picture → *Settings* → *Phone verification*) - do this once, before the session.
2. Click **Create → New Notebook**.
3. In the notebook editor: **File → Import Notebook**. Either upload the `.ipynb` file downloaded from GitHub, or paste the
   GitHub link of the notebook. (The *Kaggle* link in the [README](README.md) can also open it directly.)
4. In the right-hand side panel open **Session options / Settings** and switch **Internet** to **On**.
   *Without this the data download fails.*
5. Click **Run All** (or `Shift + Enter` cell by cell).

---

## Option 3 - On your own computer

Works on Windows, macOS and Linux.

**One-time installation**
1. Install **Python 3.10 or newer** from <https://www.python.org/downloads/> (on Windows tick *"Add Python to PATH"*).
2. Download the repository: on GitHub click **Code → Download ZIP**, then unzip it. (With git:
   `git clone https://github.com/simonkng/ophthalmology-ml-workshop.git`)
3. Open a terminal (Windows: *PowerShell*; macOS: *Terminal*) and go into the unzipped folder:
   ```bash
   cd ophthalmology-ml-workshop
   ```
4. Create an isolated environment and install the libraries:

   macOS / Linux
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```
   Windows (PowerShell)
   ```powershell
   py -m venv .venv
   .venv\Scripts\Activate.ps1
   pip install -r requirements.txt
   ```

**Every time you want to work**
```bash
cd ophthalmology-ml-workshop
source .venv/bin/activate        # Windows: .venv\Scripts\Activate.ps1
jupyter lab
```
Your browser opens Jupyter Lab. In the file list open `notebooks/session1/...ipynb` (or `session2`) and use
**Run → Run All Cells**.

*Alternative:* Anaconda users can run `pip install -r requirements.txt` in their Anaconda environment and start Jupyter from
Anaconda Navigator; VS Code with the *Jupyter* extension also works.

---

## Troubleshooting

| Problem | What to do |
|---|---|
| `URLError` / `HTTP Error` / timeout in the first data cell | No internet or the site is blocked. Check your connection, on Kaggle switch **Internet → On**, then re-run the cell. |
| No internet in the session at all | Download the CSV in a browser on a connected device: <https://huggingface.co/datasets/harvardairobotics/Harvard-GDP/resolve/main/ReadMe/data_summary.csv>, upload it to Colab / Kaggle / the notebook folder, and in the data cell replace the long URL in `GDP_URL = "..."` by the file name `"data_summary.csv"`. Do not share the CSV further (license). |
| `ModuleNotFoundError: No module named ...` | Run `pip install -r requirements.txt` (local) or `!pip install seaborn scikit-learn` in a cell (Colab / Kaggle), then re-run. |
| A cell shows an error after changing something | **Runtime / Kernel → Restart and run all**. |
| Numbers differ slightly from the slides | Different library versions can change small decimals; the message stays the same. A fixed random seed is used wherever possible. |
| Plots do not appear | Run the setup cell first; in Jupyter Lab use *Kernel → Restart Kernel and Run All Cells*. |

Questions: simon.koenig@unimedizin-mainz.de (or via the workshop organisers).

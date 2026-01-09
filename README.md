# Causal Inference in Python
**NCG613: Data Analytics Project**  
Kevin Credit  
2026

## Overview

This repository contains lab materials for NCG613: Data Analytics Project at Maynooth University. The practicals contained here cover data analytics and causal inference methods using Python on open data.

![Course Image](/Users/kevincredit/Library/CloudStorage/OneDrive-MaynoothUniversity/NCG613/NCG613/Image.png)

## Quick Start

### 1. Get Your Own Copy of the Repository

**Important:** This repository is for distribution of course materials. You should create your own personal copy to work with (not edit the main repository directly).

#### Option A: Fork the Repository (Recommended if you use GitHub)

1. Click the **"Fork"** button at the top-right of this GitHub page
2. This creates your own copy under your GitHub account
3. Clone YOUR fork to your computer (see cloning instructions below)
4. Work in your fork - you can make any changes you want!

#### Option B: Download as ZIP (Simplest for beginners)

1. Click the green **"Code"** button at the top of this page
2. Select **"Download ZIP"**
3. Extract the ZIP file to a location on your computer (e.g., Documents/Courses/)
4. You now have your own local copy to work with!

#### Option C: Clone Directly (For distribution only)

If you just want to follow along without making changes:

**Using GitHub Desktop:**
1. Download [GitHub Desktop](https://desktop.github.com/)
2. Sign in with your GitHub account
3. File → Clone Repository → URL tab
4. Enter: `https://github.com/kcredit/NCG613`
5. Choose save location → Click "Clone"

**Using command line:**
```bash
git clone https://github.com/kcredit/NCG613.git
cd NCG613
```

### 2. Download Required Large Data File

One data file is too large for GitHub and must be downloaded separately from Zenodo:

**Required file:** `OutputAreas.geojson` (used in Practicals 7, 8, and 9)

**Download instructions:**

1. Visit: https://zenodo.org/records/18198787
2. Click **"Download"** next to `OutputAreas.geojson` (or download all files)
3. Save the file to the `data/` folder in your course directory
4. Final location should be: `NCG613/data/OutputAreas.geojson`

**File details:**
- Size: 298 MB
- Format: GeoJSON
- Contents: Output Area boundaries for London with census data
- Required for: Practicals 7, 8, and 9

### 3. Set up your Python environment

After getting your copy and downloading the data file, install the required Python packages:

**Option A: Using Anaconda Navigator (Easiest for beginners)**

Anaconda provides a user-friendly interface for managing Python. You'll need to use the command line briefly for installation, but Navigator handles everything else:

1. Download and install [Anaconda](https://www.anaconda.com/download/)
2. Open **Anaconda Navigator** (find it in your applications)
3. Click **Environments** (left sidebar) → **Create** button (bottom)
   - Name: `NCG613`
   - Python version: 3.10 or higher
   - Click **Create**
4. With `NCG613` environment selected, click the ▶️ button → **Open Terminal**
5. In the terminal window that opens, run these two commands:

   ```bash
   cd path/to/NCG613
   pip install -r requirements.txt
   ```
   
   *Tip: Replace `path/to/NCG613` with the actual path where you saved the course files. See below for more detail.*
   
6. Wait for installation to complete (may take 5-10 minutes), then close the terminal
7. Back in Navigator, click **Home** (left sidebar)
8. Select `NCG613` from the dropdown at top (important!)
9. Click **Launch** under Jupyter Notebook
10. Navigate to `notebooks/` folder and start working!

*Once set up, you'll only use Navigator's buttons - no more command line needed for daily use.*

**Option B: Command line only (For users comfortable with terminal/command prompt)**

```bash
# Navigate to your copy of the repository
cd `path/to/NCG613`

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install required packages
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

*This is faster to set up but requires command line comfort. You'll use terminal commands each time you work.*

#### How to Find the Path for the `cd` Command

##### Easy Method: Get the Path from Finder/Explorer

###### On Mac:

1. **Open Finder**
2. Navigate to where you saved NCG613 folder
3. **Right-click (or Control+click)** on the NCG613 folder
4. Select **New Terminal at Folder**
5. The terminal window that opens will be set to that location

**Alternative Mac method:**

1. Find the NCG613 folder in Finder
2. **Drag and drop** the folder into Terminal after typing `cd `
3. The path appears automatically!

##### On Windows:

1. **Open File Explorer**
2. Navigate to where you saved NCG613 folder
3. Click on the **address bar** at the top (shows the path)
4. Press **Ctrl+C** to copy
5. In Command Prompt, type: `cd ` (with a space) then **Ctrl+V**

**Alternative Windows method:**

1. Navigate to NCG613 folder in File Explorer
2. Click in the address bar and type `cmd`
3. Press Enter
4. Command Prompt opens **already in that directory!** (no cd needed)

#### If You Used GitHub Desktop

Even easier:

1. Open **GitHub Desktop**
2. Make sure NCG613 repository is selected (dropdown at top-left)
3. Click **Repository** menu → **Open in Terminal** (Mac) or **Open in Command Prompt** (Windows)
4. Terminal opens **already in the right directory!**

#### Common Locations

Your NCG613 folder is likely in one of these places:

**Mac:**
```bash
cd ~/Documents/NCG613
cd ~/Desktop/NCG613
cd ~/Documents/GitHub/NCG613
```

**Windows:**
```bash
cd C:\Users\YourUsername\Documents\NCG613
cd C:\Users\YourUsername\Desktop\NCG613
cd C:\Users\YourUsername\Documents\GitHub\NCG613
```

Replace `YourUsername` with your actual Windows username.

### 4. Daily Workflow: Opening Notebooks Again

**If you used Option A (Anaconda Navigator):**

Every time you want to work on the practicals:
1. Open **Anaconda Navigator**
2. Make sure **`NCG613` is selected** in the dropdown at the top (this activates your environment)
3. Click **Launch** under Jupyter Notebook
4. Navigate to `notebooks/` and open your files

**If you used Option B (Command line):**

Every time you want to work:
```bash
cd path/to/NCG613
source venv/bin/activate  # On Windows: venv\Scripts\activate
jupyter notebook
```

⚠️ **Important:** Always make sure your environment is activated (Option A) or your virtual environment is active (Option B) before launching Jupyter. This ensures all the required packages are available!

## Getting Updates from the Instructor

When new materials are added to the main repository, you can update your copy:

**If you forked the repository on GitHub:**

Your fork doesn't automatically update. To get new materials:

1. Go to YOUR fork on GitHub
2. Click "Sync fork" → "Update branch"
3. Then pull the changes to your local copy:
   - **GitHub Desktop:** Click "Fetch origin" → "Pull origin"
   - **Command line:** `git pull`

**If you downloaded as ZIP:**

Simply download the latest ZIP file again and extract it (or just download new individual files you need).

**If you cloned directly (Option C above):**

```bash
cd NCG613
git pull
```

## Repository Structure

```
NCG613/
├── notebooks/         # Jupyter notebooks for practicals
├── data/              # Course datasets
│   ├── hpdemo.csv
│   ├── OutputAreas.geojson  # ← Download this from Zenodo!
│   └── ...
├── README.md          # This file
└── requirements.txt   # Python dependencies
```

## Course Materials

### Notebooks

- **Practical 1**: Python Basics for Data Analytics
- **Practical 6**: Mapping and Exploring Spatial Data
- **Practical 7**: Regression Models for Spatial Data
- **Practical 8**: Statistical Causal Inference
- **Practical 9**: Causal Machine Learning in CausalML

### Data Files

Most data files are included in the repository. However:

**✓ Included in repository:**
- `hpdemo.csv`
- All small data files (<100 MB)

**⚠️ Download separately from Zenodo:**
- `OutputAreas.geojson` → https://zenodo.org/records/18198787
  - **Required for Practicals 7, 8, and 9**
  - Place in `data/` folder after downloading

All notebooks use relative paths (e.g., `../data/hpdemo.csv`) so they'll work once files are in the correct locations.

## Working with the Materials

### Running Notebooks Locally

1. Open Anaconda Navigator (or use command line)
2. Select the `NCG613` environment
3. Launch Jupyter Notebook
4. Navigate to the `notebooks/` folder
5. Click on any `.ipynb` file to open and run it

### Jupyter Tips

- Press `Shift + Enter` to run a cell
- Press `Esc` then `A` to insert a cell above
- Press `Esc` then `B` to insert a cell below
- Press `Esc` then `DD` to delete a cell
- Click "Kernel" → "Restart & Clear Output" to start fresh

## Troubleshooting

### "OutputAreas.geojson not found" error

**Solution:** Download the file from Zenodo (see Section 2 above) and place it in the `data/` folder.

### Package installation fails

**Solution:** 
1. Make sure you're using Python 3.10 or higher: `python --version`
2. Try installing packages one at a time to identify which is failing
3. Check that you have sufficient disk space (~2-3 GB needed)
4. On Windows, you may need to install [Visual C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

### Jupyter kernel keeps dying

**Solution:**
1. Restart the kernel: Kernel → Restart
2. Check available RAM (some spatial operations need 4-8 GB)
3. Try running cells one at a time rather than "Run All"

### Can't find conda/anaconda command

**Solution:** 
1. Close and reopen your terminal/command prompt
2. Or use Anaconda Navigator instead of command line
3. On Mac/Linux, run: `source ~/anaconda3/bin/activate`

## Software Requirements

- Python 3.10+
- Jupyter Notebook or JupyterLab
- Required packages are listed in `requirements.txt`
- ~3-4 GB free disk space for packages and data
- ~4-8 GB RAM recommended for spatial analysis

## Getting Help

If you encounter issues:

1. Check the **Troubleshooting** section above
2. Ensure all requirements are installed: `pip list | grep [package-name]`
3. Make sure `OutputAreas.geojson` is downloaded and in the `data/` folder
4. Try restarting the Jupyter kernel
5. Consult the course Moodle page
6. Ask in class or during office hours

## Additional Resources

- [Python Documentation](https://docs.python.org/3/)
- [Jupyter Documentation](https://jupyter.org/documentation)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [GeoPandas Documentation](https://geopandas.org/)
- [Anaconda Documentation](https://docs.anaconda.com/)
- [GitHub Guides](https://guides.github.com/)

## For Instructors: Contributing Changes

This section is for instructors or collaborators who want to contribute improvements:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature-name`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin feature-name`)
6. Create a Pull Request

Students should **not** submit pull requests - instead, work in your own fork or local copy!

## License

MIT License

Copyright (c) 2026 Kevin Credit

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Acknowledgments

Course materials developed by Kevin Credit for NCG613: Data Analytics Project at Maynooth University. Some materials adapted from exercises originally created by Prof. Chris Brunsdon.

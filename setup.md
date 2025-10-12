## Installation using your Local Environment

### Step 1: Install VS Code. 

Download from [Visual Studio Code](https://code.visualstudio.com/Download)

### Step 2: Install Python 3

Download from [Python](https://www.python.org/downloads/)

- Check version:
```bash
python3 --version
```

### Step 3: Clone this repository:
```bash
git clone https://github.com/yourusername/pandas-comprehensive-tutorial.git
cd pandas-comprehensive-tutorial
```
Replace `yourusername` with your actual GitHub username.

### Step 4: Create a Virtual Environment
A virtual environment is like a **sandbox** for your Python project. Instead of installing all packages globally in your system, you isolate them for each project.

Open Terminal in your project folder:
```bash
python3 -m venv myenv
```

**Activate** it:

- On windows:
```bash
myenv\Scripts\activate
```

- On macOS/Linux:
```bash
source myenv/bin/activate
```
You’ll see `(myenv)` in your terminal when it’s active.

To **deactivate** the virtual environment, run:

- On Windows:
```bash
myenv\Scripts\deactivate.bat
```

- On macOS/Linux:
```bash
deactivate
```

*Here’s why it matters to use a **virtual environment**:*

1. **Avoid version conflicts**

- Project A needs `pandas==1.5.3`

- Project B needs `pandas==2.2.2`

    If you install globally, they’ll overwrite each other. In a virtual environment, each project has its own version.

2. **Reproducibility**

- You can freeze dependencies in a `requirements.txt` file.

- Later, you (or teammates) can recreate the *exact same environment* anywhere.

3. **Keep your system clean**

- Installing everything globally can pollute your system with unused packages.

- If something breaks, you don’t need to reinstall Python, just delete the environment and recreate it.

4. **Industry standard**

- Almost every Python job/project uses virtual environments (`venv`, `conda`, `poetry`, etc.).

- Makes collaboration much smoother.

In short: **Virtual environments = Stability + Clean projects + No conflicts**.


### Step 5: Install required packages:
Inside your **activated myenv**, install the necessary libraries from the `requirements.txt` file:
```bash
pip install -r requirements.txt
```
Or manually:

```bash
pip install pandas numpy pyarrow notebook jupyter
```

### Step 6: Install VS Code Extensions
In VS Code, open the Extensions Marketplace and install:

- Python (Microsoft)
- Jupyter (Microsoft)

### Step 7: Launch Jupyter notebook:
1. Open VS Code → File > Open Folder → select your project.

2. Open your `pandas_comprehensive_tutorial.ipynb` file.

3. VS Code will show it in Notebook Editor mode.

4. At the top right, click “Select Kernel” → choose the Python environment from your `myenv`.

### Step 8: Run!
- Use the ▶ Run button next to each cell.

- Or press Shift+Enter to run a cell.

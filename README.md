# Pandas Comprehensive Tutorial

A complete walkthrough of essential pandas operations for data manipulation and analysis. This Jupyter notebook covers fundamental to advanced pandas functionality with practical examples using real datasets.

## 📋 Table of Contents

- [Overview](#overview)
- [Datasets Used](#datasets-used)
- [Topics Covered](#topics-covered)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Key Learning Points](#key-learning-points)
- [Performance Tips](#performance-tips)
- [Contributing](#contributing)

## 🎯 Overview

This tutorial provides hands-on experience with pandas, covering everything from basic data loading to advanced operations like merging, aggregation, and time series manipulation. The notebook is structured progressively, making it suitable for both beginners and intermediate users looking to strengthen their pandas skills.

## 📊 Datasets Used

The tutorial uses three main datasets:
- **Coffee Sales Data**: Daily coffee shop sales with different coffee types
- **Biographical Data**: Olympic athletes' biographical information
- **Country Codes**: NOC (National Olympic Committee) to country name mappings

All datasets are loaded directly from GitHub repositories, so no local files are required.

## 📚 Topics Covered

### 1. **Data Loading**
- CSV vs Parquet formats
- Performance considerations
- Remote data loading

### 2. **Data Access & Selection**
- `.loc` vs `.iloc` indexing
- Row and column selection
- Best practices for data access

### 3. **Data Filtering**
- Boolean indexing
- String operations with `.str` accessor
- Multiple condition filtering
- Performance comparison of filtering methods

### 4. **Column Operations**
- Adding new columns
- Conditional column creation (`np.where`, `np.select`, `pd.cut`)
- Data type conversions
- Performance optimization techniques

### 5. **Data Export**
- CSV export options
- Index handling

### 6. **Merging & Concatenation**
- Different join types
- Data combination strategies
- Post-merge data cleaning

### 7. **Null Value Handling**
- Detection methods
- Filling strategies
- Dropping vs filling approaches

### 8. **Data Aggregation**
- GroupBy operations
- Value counts
- Statistical summaries

### 9. **Advanced Functionality**
- Shift operations for lag variables
- Ranking systems
- Cumulative operations

## 🔧 Prerequisites

- Basic Python knowledge
- Understanding of data structures (lists, dictionaries)
- Familiarity with Jupyter notebooks

## 🚀 Installation

### Using Google Colab
Download the `pandas_comprehensive_tutorial.ipynb` file. Go to [Google Colab](https://colab.research.google.com/) and upload it.

### Using your Local Environment

#### Step 1: Install VS Code. 

Download from [Visual Studio Code](https://code.visualstudio.com/Download)

#### Step 2: Install Python

Download from [Python](https://www.python.org/downloads/)

- Check version:
```bash
python3 --version
```

#### Step 3: Clone this repository:
```bash
git clone https://github.com/yourusername/pandas-comprehensive-tutorial.git
cd pandas-comprehensive-tutorial
```
Replace `yourusername` with your actual GitHub username.

#### Step 4: Create a Virtual Environment
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


#### Step 5: Install required packages:
Inside your **activated myenv**, install the necessary libraries from the `requirements.txt` file:
```bash
pip install -r requirements.txt
```
Or manually:

```bash
pip install pandas numpy pyarrow notebook jupyter
```

#### Step 7: Install VS Code Extensions
In VS Code, open the Extensions Marketplace and install:

- Python (Microsoft)
- Jupyter (Microsoft)

#### Step 7: Launch Jupyter notebook:
1. Open VS Code → File > Open Folder → select your project.

2. Open your `pandas_comprehensive_tutorial.ipynb` file.

3. VS Code will show it in Notebook Editor mode.

4. At the top right, click “Select Kernel” → choose the Python environment from your `myenv`.

#### Step 8: Run!
- Use the ▶ Run button next to each cell.

- Or press Shift+Enter to run a cell.

## 📖 Usage

The notebook is designed to be run cell by cell. Each section builds upon the previous one, so it's recommended to execute cells in order. Key features:

- **Interactive Examples**: All code can be executed immediately
- **Real Data**: Uses actual datasets for practical learning
- **Performance Notes**: Includes optimization tips and best practices
- **Comprehensive Comments**: Every operation is explained

## 💡 Key Learning Points

### Performance Best Practices
- Use vectorized operations over `.apply()` when possible
- Prefer `.loc` for explicit, readable code
- Choose appropriate data types for memory efficiency
- Use `pd.cut()` for binning operations instead of nested conditions

### Code Quality
- Always use `.copy()` when creating DataFrame variants
- Handle null values explicitly
- Use descriptive column names
- Prefer explicit over implicit operations

### Data Manipulation Patterns
- **Split-Apply-Combine** pattern with GroupBy
- **Conditional Logic** with `np.where()`, `np.select()`, and `pd.cut()`
- **Data Integration** with merge and concatenate operations

## ⚡ Performance Tips

1. **Use `pd.cut()` instead of `apply()` for categorization** - Up to 100x faster
2. **Prefer `np.select()` over nested `np.where()`** - Cleaner and faster
3. **Use appropriate data types** - Can reduce memory usage by 90%
4. **Filter before operations** - Reduce computational overhead

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Add new examples
- Improve existing explanations
- Fix bugs or typos
- Suggest performance improvements

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Data sources from [Keith Galli's pandas tutorial repository](https://github.com/KeithGalli/complete-pandas-tutorial.git)
- Pandas development team for creating this amazing library
- The open-source community for continuous improvements

---

**Happy Data Engineering!** 🐼📊
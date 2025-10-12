# Pandas Comprehensive Tutorial

This is a concise demonstration of essential pandas operations for data manipulation and analysis.

This tutorial covers: 
- reading data (*CSV and Parquet formats*) and some performance considerations, 
- accessing data and some best practices,
- filtering data and a performance comparison,
- column operations such as adding new columns, naming, and datatype conversions,
- data export options,
- merging (*join types*) and concat data, 
- handling null values,
- aggregating data (*groupBy operations*), and
- some advance functionality (*shift operations, ranking systems, cumulative operations, ...*).


## About the datasets

The tutorial uses three main datasets:
- **Coffee Sales Data**: Daily coffee shop sales with different coffee types
- **Biographical Data**: Olympic athletes' biographical information
- **Country Codes**: NOC (National Olympic Committee) to country name mappings

All datasets are loaded directly from GitHub repositories, so no local files are required.

## Prerequisites

- Basic Python knowledge
- Understanding of data structures (lists, dictionaries)
- Familiarity with Jupyter notebooks

## Installation

### Using Google Colab
Download the `pandas_comprehensive_tutorial.ipynb` file. Go to [Google Colab](https://colab.research.google.com/) and upload it.

### Using your Local Environment

Read the instructions from [setup.md](./setup.md)

## Key Learning Points

### Performance Best Practices
- Use vectorized operations over `.apply()` when possible
- Prefer `.loc` for explicit, readable code
- Choose appropriate data types for memory efficiency
- Use `pd.cut()` for binning operations instead of nested conditions

### Code Quality
- Use `.copy()` when creating DataFrame variants to avoid *name binding*
- Handle null values explicitly
- Use descriptive column names
- Prefer explicit over implicit operations

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Data sources from [Keith Galli's pandas tutorial repository](https://github.com/KeithGalli/complete-pandas-tutorial.git)
- Pandas development team for creating this amazing library
- The open-source community for continuous improvements

---

**Happy Data Engineering!** 🐼📊
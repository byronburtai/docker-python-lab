# 🧪 Dockerized Python Lab with Jupyter

A modular, restartable Python lab powered by Docker and JupyterLab. Includes mock business data, mounted folders, and zero-token access for frictionless local development.

## 🚀 Features

- JupyterLab served via Docker
- No token or password required
- Mounted `notebooks/` and `data/` folders
- Sample business dataset (`sample.csv`) included
- Clean `.gitignore` for version control hygiene

## 📁 Folder Structure

```
docker-python-lab/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── main.py
├── notebooks/
│   └── test-lab.ipynb
├── data/
│   └── sample.csv
├── .gitignore
├── README.md
```

## 🧭 Quick Start

Clone the repo and launch the lab:

```bash
git clone https://github.com/byronburtai/docker-python-lab.git
cd docker-python-lab
docker-compose up
```

Then open [http://localhost:8888](http://localhost:8888) in your browser.

## 📊 Sample Dataset

`data/sample.csv` contains mock business sales data:

| date       | product_id | product_name         | units_sold | unit_price | total_revenue |
|------------|------------|----------------------|------------|------------|----------------|
| 2025-09-01 | P001       | Wireless Mouse       | 12         | 25.99      | 311.88         |
| 2025-09-02 | P003       | Mechanical Keyboard  | 5          | 89.99      | 449.95         |

## 🧪 Notebook Preview

The included notebook (`test-lab.ipynb`) demonstrates:

```python
import pandas as pd

df = pd.read_csv('../data/sample.csv')
summary = df.groupby('product_name')['total_revenue'].sum()
summary.plot(kind='bar')
```

## 🛡️ .gitignore Highlights

```txt
__pycache__/
.ipynb_checkpoints/
.env
output/
```

## 📦 Requirements

```txt
jupyterlab
pandas
matplotlib
```

## 🧱 Built By

Byron Burt — [github.com/byronburtai](https://github.com/byronburtai)  
Focused on modular, restartable environments and clean deployment workflows.
```
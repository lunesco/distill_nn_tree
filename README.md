# Wymagania
1. Pobieramy [Python 3.8.7](https://www.python.org/downloads/release/python-387/) i instalujemy. 
2. Pobieramy [git](https://git-scm.com/downloads) i instalujemy.
3. Pobieramy [git-lfs](https://git-lfs.github.com/), który przechowuje duże pliki. Następnie uruchamiamy komendy:
```
git lfs install
git lfs pull
```

## Windows 10
Tworzymy wirtualne środowisko:
```
py -3.8 -m venv venv
.\venv\Scripts\activate
py -3.8 -m pip install -r requirements.txt
```

## Linux
Tworzymy wirtualne środowisko:
```
python3.8 -m venv venv
. /venv/bin/activate
python3.8 -m pip install -r requirements.txt
```

## Results
The table below summarizes results as produced and presented in [mnist.ipynb](mnist.ipynb), but no exhaustive hyperparameter search was performed, so there is space for improvement.

| Model          | Depth | Labels | Batch size | Epochs | Accuracy |
|----------------|-------|--------|------------|--------|----------|
| ConvNet        | -     | hard   | 16         | 12     | 99.27%   |
| Tree (normal)  | 4     | hard   | 4          | 40     | 90.59%   |
| Tree (distill) | 4     | soft   | 4          | 40     | 92.24%   |


# ASI Project – Mushroom Classification

Projekt z uczenia maszynowego dotyczący klasyfikacji grzybów na **jadalne** i **trujące** na podstawie zbioru danych *Mushroom Dataset*.

---

## Dataset

**Źródło**:  
https://archive.ics.uci.edu/dataset/73/mushroom

**Licencja**:  
Creative Commons Attribution 4.0 International (CC BY 4.0)  
https://creativecommons.org/licenses/by/4.0/

**Data pobrania**:  
15.10.2025

---

## Metryka

**F1-score dla klasy `poisonous`**

Uzasadnienie:  
Błąd polegający na sklasyfikowaniu trującego grzyba jako jadalny jest krytyczny, dlatego metryka F1-score pozwala zbalansować precyzję i recall dla klasy trujących grzybów.

---

## Weights & Biases

Dashboard eksperymentów:  
https://wandb.ai/s25983-pjatk/mushrooms?nw=nwusers25983

---

## Wymagania

- Git  
- Conda lub Miniconda  
- Python 3.9–3.11  

---

## Uruchomienie projektu

### 1. Sklonuj repozytorium

```bash
git clone https://github.com/wydraaapw/ASI-Project.git
cd ASI-Project
```

### 2. Utwórz środowisko Conda

```bash
conda env create -f environment.yml
conda activate asi-ml
```

### 3. Zainstaluj projekt

```bash
pip install -e .
```

### 4. Przygotuj dane

1. Pobierz pełny zestaw danych z pierwszej linii tego pliku:  
   https://archive.ics.uci.edu/dataset/73/mushroom

2. Rozpakuj archiwum.

3. Umieść plik:

```text
agaricus-lepiota.data
```

w katalogu:

```text
data/01_raw/
```

pod nazwą:

```text
mushrooms.csv
```

---

## Uruchamianie eksperymentów Kedro

```bash
kedro run --params autogluon.time_limit=60
```

```bash
kedro run --params autogluon.time_limit=120
```

```bash
kedro run --params autogluon.presets=best_quality,autogluon.time_limit=60
```

---

## Tabela runów

![Tabela runów](https://github.com/user-attachments/assets/8234949b-df94-4699-be7c-96a123297986)

---

## Przykładowy widok W&B

![W&B view](https://github.com/user-attachments/assets/bd8a62e7-3509-4a4a-914a-7496292aff10)

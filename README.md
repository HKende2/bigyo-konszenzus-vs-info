# Konszenzus vs. információtartalom

Ez a repository a motívumkeresési összehasonlító projekt környezetét készíti elő.
A konkrét algoritmus implementációja ebben a lépésben még nincs elkezdve.

## Projektmappák

- `docs/` - célkitűzés, feladatleírás és módszertani specifikáció
- `notebooks/` - Colab/Jupyter notebook(ok)
- `data/synthetic/` - szintetikus szekvenciák és metaadatok
- `results/figures/` - ábrák (boxplot stb.)
- `results/tables/` - összesítő táblázatok (medián, IQR, elvárt-kapott)
- `reports/` - rövid jelentés(ek)

## Gyors indulás

1. Python virtual environment létrehozása:
   - Windows (bash): `python -m venv .venv && source .venv/Scripts/activate`
2. Függőségek telepítése:
   - `pip install -r requirements.txt`
3. Notebook megnyitása:
   - `notebooks/konszenzus_vs_informaciotartalom_colab.ipynb`

## Megjegyzés

A részletes célkitűzések és elfogadási feltételek a `docs/celkituzesek.md` fájlban találhatók.

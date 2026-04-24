# Predikce výsledků závodů Formule 1 pomocí strojového učení

Tento repozitář slouží jako příloha k bakalářské práci **Predikce výsledků závodů Formule 1 pomocí strojového učení**.

Obsahuje Jupyter Notebook se zdrojovým kódem použitým pro zpracování dat, tvorbu prediktorů, trénování modelů, evaluaci a interpretaci výsledků. Součástí repozitáře jsou také datové soubory použité v notebooku.

## Struktura repozitáře

```text
.
├── README.md
├── f1_predictions_bp.ipynb
└── f1_data/
    ├── circuits.csv
    ├── constructor_standings.csv
    ├── constructors.csv
    ├── driver_standings.csv
    ├── drivers.csv
    ├── lap_times.csv
    ├── pit_stops.csv
    ├── pitstops_old.csv
    ├── qualifying.csv
    ├── races.csv
    ├── results.csv
    ├── safety_cars.csv
    ├── status.csv
    └── weather_features_v4.csv
```

## Hlavní notebook

Soubor `f1_predictions_bp.ipynb` obsahuje kompletní postup praktické části práce, zejména:

- načtení a kontrolu dat,
- spojení jednotlivých datových zdrojů,
- předzpracování dat,
- exploratorní datovou analýzu,
- tvorbu cílové proměnné a prediktorů,
- rozdělení dat na trénovací a testovací sadu,
- trénování modelů strojového učení,
- ladění hyperparametrů,
- evaluaci modelů,
- interpretaci výsledků.

## Použitá data

Datové soubory jsou uloženy ve složce `f1_data/`. Notebook k nim přistupuje pomocí relativních cest ve tvaru `f1_data/nazev_souboru.csv`, proto je nutné zachovat uvedenou strukturu složek.

Použité soubory pocházejí z veřejně dostupných zdrojů na platformě Kaggle a obsahují historická data o závodech Formule 1, výsledcích jezdců, kvalifikacích, zastávkách v boxech, výjezdech safety caru a počasí.

Hlavní skupiny použitých dat:

- základní informace o závodech, okruzích, jezdcích a konstruktérech,
- výsledky závodů a kvalifikací,
- průběžná pořadí jezdců a konstruktérů,
- časy kol a zastávky v boxech,
- historická data o výjezdech safety caru,
- počasí při závodech.

Pro účely modelování byla data v práci omezena na sezony 2010–2025.

## Modely

V práci byly porovnány následující modely strojového učení:

- rozhodovací strom,
- náhodný les,
- XGBoost,
- CatBoost,
- neuronová síť.

Cílová proměnná byla definována jako vícetřídní klasifikace výsledku pilota v závodě do čtyř tříd:

- Vítězství,
- Pódium,
- Body,
- Bez bodů.

## Reprodukovatelnost

Analýza byla provedena v jazyce Python 3.11.7. Konkrétní verze hlavních použitých knihoven jsou uvedeny v textu bakalářské práce.

Pro spuštění notebooku je třeba zachovat strukturu repozitáře, zejména umístění datových souborů ve složce `f1_data/`.

## Autor

Petr Horák  
Fakulta informatiky a statistiky  
Vysoká škola ekonomická v Praze  
2026

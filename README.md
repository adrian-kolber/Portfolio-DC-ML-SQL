# Analiza jakości powietrza w Krakowie

> Jak zmieniała się jakość powietrza w Krakowie w latach 2016–2025 i kiedy ryzyko związane z zanieczyszczeniem jest najwyższe?

Projekt eksploracyjnej analizy danych środowiskowych dla stacji **Kraków, os. Piastów**. Analiza obejmuje dzienne wskaźniki AQI dla pyłów zawieszonych i gazów oraz pokazuje sezonowość, współwystępowanie zanieczyszczeń i długoterminowe zmiany jakości powietrza.

## Cele projektu

- Zbadać zmienność jakości powietrza w czasie.
- Określić miesiące, w których jakość powietrza jest najsłabsza.
- Sprawdzić, które zanieczyszczenia najczęściej wpływają na ogólny wskaźnik AQI.
- Porównać rozkład kategorii jakości powietrza między latami.
- Przedstawić wnioski w formie czytelnych wykresów.

## Dane

- **Lokalizacja:** Kraków, os. Piastów, Małopolska, Polska
- **Zakres:** 23 stycznia 2016 – 8 listopada 2025
- **Częstotliwość:** obserwacje dzienne
- **Plik:** [`data.csv`](data.csv)

Zbiór zawiera indywidualne wskaźniki AQI dla:

| Kolumna | Zanieczyszczenie |
| --- | --- |
| `pm25` | pył zawieszony PM2.5 |
| `pm10` | pył zawieszony PM10 |
| `o3` | ozon |
| `no2` | dwutlenek azotu |
| `so2` | dwutlenek siarki |
| `co` | tlenek węgla |

Źródła danych: dane stacji publikowane przez GIOŚ/WIOŚ Kraków oraz [AQICN](https://aqicn.org/).

## Metodyka

W analizie:

1. Wczytano i przygotowano dane czasowe w Pandas.
2. Zidentyfikowano oraz obsłużono brakujące obserwacje.
3. Utworzono złożony wskaźnik AQI jako maksimum dostępnych wskaźników dla danego dnia.
4. Przeanalizowano trendy dzienne, miesięczne i roczne.
5. Zbadano korelacje pomiędzy zanieczyszczeniami.
6. Przypisano dni do kategorii jakości powietrza według skali AQI.

> **Uwaga interpretacyjna:** część substancji nie była mierzona przez cały okres analizy. Wyniki, zwłaszcza porównania najwcześniejszych lat, należy interpretować z uwzględnieniem dostępności pomiarów.

## Najważniejsze elementy analizy

- Trend PM2.5 i złożonego AQI w latach 2016–2025.
- Sezonowość jakości powietrza na podstawie median miesięcznych.
- Macierz korelacji wskaźników AQI.
- 30-dniowa średnia krocząca, ułatwiająca odczyt długoterminowego trendu.
- Rozkład kategorii AQI oraz porównanie liczby dni w każdej kategorii między latami.

## Wnioski

Analiza wskazuje na wyraźną sezonowość: najsłabsza jakość powietrza przypada na okres grzewczy. Pyły zawieszone są istotnym czynnikiem wpływającym na wysokie wartości AQI, a porównanie kategorii jakości powietrza między latami pozwala ocenić kierunek zmian w czasie.

Szczegółowe wykresy, obliczenia i interpretacje znajdują się w notebooku.

## Uruchomienie projektu

1. Sklonuj repozytorium:

   ```bash
   git clone https://github.com/adrian-kolber/Portfolio-DC-ML-SQL.git
   cd Portfolio-DC-ML-SQL
   ```

2. Utwórz środowisko i zainstaluj biblioteki:

   ```bash
   python -m venv .venv
   # Windows
   .venv\\Scripts\\activate
   # macOS/Linux
   source .venv/bin/activate

   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Otwórz notebook:

   ```bash
   jupyter notebook "air pollution Krakow.ipynb"
   ```

## Technologie

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

## Pliki

| Plik | Opis |
| --- | --- |
| [`air pollution Krakow.ipynb`](air%20pollution%20Krakow.ipynb) | pełna analiza i wizualizacje |
| [`data.csv`](data.csv) | dzienne dane AQI |

---

Projekt wykonany jako element portfolio Data Science.

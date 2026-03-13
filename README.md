# mini-automl-system

### Project overview
Projekt stanowi uproszczony system AutoML dedykowany do klasyfikacji binarnej na danych tabelarycznych. Głównym celem pracy było stworzenie stabilnego systemu, który automatycznie wybiera optymalne modele oraz wykorzystuje techniki ensemblingu do poprawy jakości predykcji.

### Key features
Model screening: portfolio 50 zróżnicowanych konfiguracji modeli.
Zautomatyzowany pipeline: automatyczna obsługa braków danych, skalowanie oraz kodowanie zmiennych kategorycznych.
Selekcja: wybór top-5 modeli na podstawie 5-krotnej walidacji krzyżowej z metryką balanced accuracy.
Ensembling: implementacja soft voting dla najlepszych modeli w celu poprawy stabilności predykcji

### Model portfolio
Zamiast kosztownych obliczeniowo sieci neuronowych, system opiera się na sprawdzonych rozwiązaniach dla danych tabelarycznych.

### Klasa MiniAutoML
Sercem systemu jest klasa MiniAutoML, która automatyzuje cykl życia modelu klasyfikacyjnego.Główne metody:
- fit(X, y): główny proces uczenia, który wykonuje: preprocessin, walidację (obliczanie balanced accuracy), trenowanie i ranking modeli z portfolio oraz trening końcowy (trenowanie najlepszych modeli na całym zbiorze treningowym)
- predict_proba(X): zwraca prawdopodobieństwo przynależności do klasy pozytywnej. W przypadku użycia ensemble, wyniki z top-5 modeli są uśredniane metodą soft voting.
- predict(X): zwraca ostateczne etykiety klas binarnych na podstawie wypracowanych prawdopodobieństw

### Struktura repozytorium
* automl.ipynb: główny notebook zawierający implementację klasy MiniAutoML oraz proces eksperymentów
* models.json: plik konfiguracyjny zawierający 50 konfiguracji modeli
* data/: zbiory danych użyte w badaniach
* Raport_mini_automl: pełny raport z projektu
* .figures/: wizualizacja eksperymentu, w tym częstość wyboru modeli

## Autorzy: Elissa Hallak, Liwia Jankowska, Julia Tomaszkiewicz 
## Data: Styczeń 2026


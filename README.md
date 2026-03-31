# 🛡️ DDoS Detection with Machine Learning

Projekt przedstawia system wykrywania ataków typu **DDoS (Distributed Denial of Service)** na podstawie analizy logów serwera oraz danych sieciowych.

---

## 📌 Opis projektu

Celem projektu jest wykrywanie anomalii w ruchu sieciowym i klasyfikacja zdarzeń jako:

* ✅ ruch normalny
* ⚠️ atak DDoS

Analiza opiera się na dwóch źródłach danych:

* logi serwera Apache
* dataset ruchu sieciowego zawierający ataki DDoS

---

## 📊 Dane

Projekt wykorzystuje następujące pliki:

### 📄 Apache.log

* logi serwera HTTP Apache
* zawierają informacje o zapytaniach (IP, timestamp, request, status)
* używane do analizy zachowania klientów

### 📄 Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv

* dataset z CICIDS2017
* zawiera cechy ruchu sieciowego (flow-based)
* obejmuje rzeczywiste scenariusze ataków DDoS

**Przykładowe cechy:**

* Flow Duration
* Total Fwd Packets
* Packet Length
* Flow Bytes/s
* Label (BENIGN / DDoS)

---

## ⚙️ Technologie

* Python 
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## 📂 Struktura projektu

```
.
├── DDoS.ipynb
├── Apache.log
├── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv
├── README.md
└── data/ (opcjonalnie)
```

---

## 🚀 Jak uruchomić

### 1. Klonowanie repozytorium

```bash
git clone https://github.com/twoj-login/twoj-repo.git
cd twoj-repo
```

### 2. Instalacja zależności

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### 3. Uruchomienie notebooka

```bash
jupyter notebook
```

Następnie otwórz plik:

```
DDoS.ipynb
```

---

## 🧠 Metodologia

Projekt obejmuje następujące etapy:

### 1. Wczytanie danych

* parsowanie logów Apache
* wczytanie datasetu CSV

### 2. Preprocessing

* czyszczenie danych
* usuwanie brakujących wartości
* normalizacja

### 3. Eksploracyjna analiza danych (EDA)

* analiza rozkładu klas
* wizualizacja cech

### 4. Trenowanie modelu

* klasyfikacja ruchu (IF, LOF)

### 5. Ewaluacja modelu

* Accuracy
* Precision / Recall

---

## 👨‍💻 Autor

Sebastian Cnotalski

---

## 📄 Licencja

MIT License

# Przygotowanie środowiska

## Wprowadzenie
Wykonaj ponisze kroki, aby mieć pewność, że wszystkie niezbędne zasoby i biblioteki będą mogły zostać uruchomione na Twoim laptopie.

## Kroki do wykonania
- [1: Sprawdź swój dostęp do platformy watsonx.ai](https://dataplatform.cloud.ibm.com/wx/home?context=wx)
- [2: Stwórz nowe wirtualne środowisko](create-virtual-python-environment.md)
- [3: Zainstaluj niezbędne biblioteki](#virtual-environment)
- [4. Uruchom plik test.py i sprawdź czy wszystko poprawnie działa](#jupyter-notebook)

### 1: Sprawdź dostęp do platformy watsonx.ai <a id="connect-to-watsonxai"></a>
Spróbuj połączyć się do platformy [watsonx.ai](https://dataplatform.cloud.ibm.com/wx/home?context=wx) z poziomu konta itz-watsonx. Jeśli nie masz dostępu, powiadom prowadzącego.

### 2: Stwórz nowe wirtualne środowisko <a id="clone-watsonxai-repo"></a>
Opis stworzenia nowego wirtualnego środowiska znajduje się [tutaj](create-virtual-python-environment.md)

### 3: Zainstaluj niezbędne biblioteki <a id="virtual-environment"></a>
Opis instalacji niezbędnych bibliotek znajduje się [tutaj](create-virtual-python-environment.md)

Jeśli instalacja wymaganych bibliotek przejdzie bez żadnych błędów, przejdz dalej.
W innym przypadku powiadom prowadzącego.

### 4: Uruchom plik test.py<a id="jupyter-notebook"></a>
Plik test.py zawiera wywołanie bibliotek, niezbędnych do przeprowadzenia laboratorium. Wywołaj plik test.py z poziomu konsoli za pomocą komendy:

```
python test.py
```
Poczekaj kilka chwil. W przypadku błędów, powiadom prowadzącego. 

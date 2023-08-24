# Stworzenie wirtualnego środowiska w Pythonie
Do stworzenia własnego wirtualnego środowiska będziemy wykorzystywać wbudowaną bibliotekę pythona - venv.

Możesz zastanawiać się dlaczego nie wykorzystujemy do tego Anacondy. Powód tej decyzji jest szczegółowo opisany pod tym linkiem [Conda/Miniconda is now on IBM's "do-not-use" list](https://w3.ibm.com/w3publisher/ossc-process/exception-and-do-not-use).

Po stworzeniu swojego własnego wirtualnego środowiska, będziesz w stanie zainstalować wszystkie wymagane biblioteki, w tym jupyter notebooka, biblioteki z Hugging Face, ChromaDB oraz biblioteki LangChain.

Otwórz Terminal i przejdź do katalogu ../workshop-watsonxai-foundations-main/labs/0-przygotowanie-środowiska i wykonaj poniższe polecenia:

```
pip install virtualenv
python -m venv watsonxai 
source watsonxai/bin/activate
pip install -r requirements_venv.txt

```
Jeśli napotkasz jakiekolwiek błędy, powiadom prowadzącego.

#### Deaktywuj swoje wirtualne środowisko
Jeśli musisz zmienić środowisko robocze, deaktywuj swoje dotychczasowe środowisko za pomocą komendy:

```
deactivate
```

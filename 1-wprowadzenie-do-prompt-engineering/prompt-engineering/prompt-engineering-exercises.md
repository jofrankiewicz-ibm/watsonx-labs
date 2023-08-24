# Prompt engineering ćwiczenia

Wykonaj poniższe ćwiczenia wykorzystując Prompt Lab z watsonx.ai.

**Ćwiczenia**
<table>
<tr>
<td><a href="#1-generate">1. Wygeneruj</a></td>
<td>Napisz trzy sentencje na temat zwierząt</td>
</tr>
<tr>
<td><a href="#2-rewrite">2. Napisz od nowa</a></td>
<td>Przekształć Markdown do HTML</td>
</tr>
<tr>
<td><a href="#3-summarize">3. Sumaryzacja</a></td>
<td>Streść historię</td>
</tr>
<tr>
<td><a href="#4-summary-points">4. Punkty podsumowujące</a></td>
<td>Stwórz listę tematów bazując na transkrypcji spotkania</td>
</tr>
<tr>
<td><a href="#5-study-questions">5. Przewidywanie pytań</a></td>
<td>Przewiduj potencjalne pytania klientów</td>
</tr>
<tr>
<td><a href="#6-text-extraction">6. Ekstrakcja tekstu</a></td>
<td>Wyodrębnij czasowniki ze zdania</td>
</tr>
<tr>
<td><a href="#7-compare">7. Porównanie</a></td>
<td>Określ, które fragmenty mają ze sobą coś wspólnego</td>
</tr>
<tr>
<td><a href="#8-text-search">8. Wyszukaj w tekście</a></td>
<td>Znajdź stronę, która zawiera poszukiwany tekst</td>
</tr>
<tr>
<td><a href="#9-classify">9. Klasyfikacja</a></td>
<td>Wykrywaj intencje użytkowników chatbota</td>
</tr>
<tr>
<td><a href="#10-anomaly-detection">10. Detekcja anomalii</a></td>
<td>Znajdź odbiegający od standardów wpis</td>
</tr>
</table>

<p>&nbsp;</p>


## 1. Wygeneruj
**Cel** 
<table>
<tr>
<td>
Napisz trzy sentencje na temat zwierząt
</td>
</tr>
</table>
  
**Przykład**
```
3 zdania o szczeniętach:
- Szczeniak kręcił się w kółko, próbując złapać się za ogon, ale skończył przewracając się w kółko.
- Jego wybryki rozśmieszyły jego właścicieli, a nawet inne szczeniaki w parku zatrzymały się, by popatrzeć na ten głupi widok.
- Gdy tylko dwa szczeniaki spotkały się w parku, zaczęły merdać ogonami i radośnie skakały wokół siebie.
```
```
3 zdania o kociakach:
- Mały kotek chłeptał mleko swoim malutkim różowym języczkiem, wydając uroczy dźwięk siorbania.
- Kociak skubał smakołyk, delektując się każdym kęsem pysznego smaku.
- Gdy tylko paczka została otwarta, oczy małego kotka zaświeciły się z podniecenia.
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#1-generate)

<p>&nbsp;</p>


## 2. Napisz od nowa
**Cel** 
<table>
<tr>
<td>
Przekształć Markdown do HTML
</td>
</tr>
</table>

**Markdown**
```
## Background
The [IBM Watson Natural Language Processing library](https://dataplatform.cloud.ibm.com/docs/
content/wsj/analyze-data/watson-nlp.html) to biblioteka Pythona, która udostępnia podstawowe elementy naturalne
przetwarzanie języka (NLP), takie jak analiza składni i ekstrakcja słów kluczowych z gotowymi rozwiązaniami,
wstępnie wytrenowane modele. Biblioteka Watson NLP ułatwia również dostosowywanie języka
modele ze słownikami terminów specyficznych dla Twojej domeny.
```
```
[MURAL](https://mural.co) to narzędzie online, które przypomina wirtualną tablicę: możesz rysować
kształty, przyklejać notatki i przenosić przedmioty. To wspaniałe narzędzie do wizualnego porządkowania pomysłów,
projektowanie rozwiązań i współpraca z członkami zespołu — w czasie rzeczywistym lub asynchronicznie.
```
```
## Function
Korzystanie z LLM jest całkiem proste: poproś model tekstem (np. „Wziąłem psa”) i model
generuje tekst jako wyjście (np. "na spacer").
```
```
## Hall of shame: when LLMs go wrong
Nawet twórcy LLM nie zawsze mogą w pełni przewidzieć lub wyjaśnić dane wyjściowe tych modeli: 
[ChatGPT's creators can’t figure out why it won’t talk about Trump](https://www.semafor.com/
article/02/03/2023/how-chatgpt-inadvertently-learned-to-avoid-talking-about-trump)
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#2-rewrite)

<p>&nbsp;</p>


## 3. Sumaryzacja
**Cel** 
<table>
<tr>
<td>
Podsumuj jedno z tych opowiadań
</td>
</tr>
</table>
  
**Short stories**

```
Mały ptaszek ćwierkał, gdy zbierała w dziobie gałązki i kawałki mchu, odlatując i
dalej między drzewami. Z każdą podróżą jej gniazdo nabierało kształtu, stając się bardziej przytulne i zachęcające.
Wkrótce stworzyła przytulny dom, w którym wychowała swoje stado ćwierkających piskląt.
```
```
Gdy tylko opakowanie zostało otwarte, oczy małego kota zaświeciły się z podniecenia. Rzuciła się
na nowej zabawce, z radością miotając nią po pokoju. Z zadowolonym mruczeniem, ona
przytuliła się do swojej zabawki, czując wdzięczność za miłość i uwagę troskliwego właściciela.
```
```
Statek kołysał się i kołysał na wzburzonym morzu, gdy szalał sztorm. Fale wysokie jak góry
uderzył w kadłub, grożąc wywróceniem się statku. Ale kapitan i załoga wytrzymali
stabilnie, poruszając się po zdradzieckich wodach z wprawą i determinacją, aż w końcu
sztorm ucichł i statek wyłonił się triumfalnie, poobijany, ale nienaruszony.
```
```
Gdy tylko dwa psy spotkały się w parku, ich ogony zaczęły machać i skakały
siebie z radością. Ich właściciele nawiązali rozmowę i wkrótce okazało się, że tak
mają ze sobą wiele wspólnego, łącząc ich wspólną miłość do psów i na zewnątrz. Do końca
dnia zawiązały się nowe przyjaźnie i zarówno psy, jak i ich właściciele opuścili park
szczęśliwe serca i merdające ogony.
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#3-summarize)

<p>&nbsp;</p>


## 4. Punkty podsumowujące
**Cel** 
<table>
<tr>
<td>
Utwórz listę tematów z jednego z tych transkrypcji spotkań
</td>
</tr>
</table>

**Transcripts**
```
00:00 [sam] Chciałem podzielić się dzisiaj najnowszymi informacjami na temat projektu X.
00:15 [sam] Projekt X zostanie zakończony pod koniec tygodnia.
00:30 [erin] To świetnie!
00:35 [erin] Słyszałem dzisiaj od klienta Y, że zgodzili się kupić nasz produkt.
00:45 [alex] Klient Z powiedział, że też to zrobią.
01:05 [sam] Wspaniałe wieści ze wszystkich stron.
```
```
00:00 [ali] Celem na dziś jest uzgodnienie rozwiązania projektowego.
00:12 [alex] Myślę, że powinniśmy rozważyć wybór 1.
00:25 [ali] Zgadzam się
00:40 [erin] Wybór 2 ma tę zaletę, że zajmie mniej czasu.
01:03 [alex] Właściwie to słuszna uwaga.
01:30 [ali] Więc co powinniśmy zrobić?
01:55 [alex] Jestem dobry z wyborem 2.
02:20 [erin] Ja też.
02:45 [ali] Gotowe!
```
```
00:00 [alex] Zaplanujmy imprezę drużynową!
00:10 [ali] Może pójdziemy na lunch do restauracji?
00:21 [sam] Dobry pomysł.
00:47 [sam] Czy my też możemy iść do kina?
01:04 [alex] Może golf?
01:15 [sam] Moglibyśmy dać ludziom możliwość zrobienia jednego lub drugiego.
01:29 [alex] Podoba mi się ten plan. Zróbmy imprezę!
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#4-summary-points)

<p>&nbsp;</p>


## 5. Przewidywanie pytań
**Goal** 
<table>
<tr>
<td>
Utwórz listę pytań, które klient może mieć na temat jednego z tych fragmentów tematycznych
</td>
</tr>
</table>

**Topic passages**

[Tworzenie notebooków](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/creating-notebooks.html)
```
Możesz dodać notatnik do swojego projektu, korzystając z jednej z następujących metod: tworząc plik notatnika,
skopiowanie przykładowego notatnika z Galerii lub dodanie notatnika z katalogu. Ty musisz mieć
rolę administratora lub redaktora w projekcie, aby utworzyć notatnik.
```
[Spark w RStudio](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/rstudio-spark.html)
```
Chociaż środowiska uruchomieniowego RStudio IDE nie można uruchomić w środowisku uruchomieniowym platformy Spark ze środowiskiem R, można użyć
Spark w skryptach języka R i aplikacjach Shiny, uzyskując programowy dostęp do jądra platformy Spark. używa RStudio
pakiet sparklyr do łączenia się ze Spark z R. Pakiet sparklyr zawiera interfejs dplyr
do ramek danych Spark, a także interfejs R do rozproszonych potoków uczenia maszynowego Spark.
```
[Narzędzie AutoAI](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-overview.html)
```
Graficzne narzędzie AutoAI w Watson Studio analizuje dane i wykrywa transformacje danych,
algorytmy i ustawienia parametrów, które najlepiej sprawdzają się w przypadku problemu z modelowaniem predykcyjnym. AutoAI
wyświetla wyniki jako modelowe potoki kandydatów uszeregowane na tablicy liderów do wyboru.
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#5-study-questions)

<p>&nbsp;</p>


## 6. Ekstrakcja tekstu
**Cel** 
<table>
<tr>
<td>
Wyodrębnij czasowniki z jednego z tych zdań
</td>
</tr>
</table>

**Sentences**
```
Gdy tylko dwa psy spotkały się w parku, ich ogony zaczęły machać i podskakiwały
wokół siebie z radością.
```
```
Ich właściciele nawiązali rozmowę i szybko odkryli, że mają ze sobą wiele wspólnego,
łącząc ich wspólną miłość do psów i na zewnątrz.
```
```
Gdy tylko opakowanie zostało otwarte, oczy małego kota zaświeciły się z podniecenia.
```
```
Rzuciła się na nową zabawkę, miotając nią po pokoju z radością.
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#6-text-extraction)

<p>&nbsp;</p>


## 7. Porównanie
**Cel** 
<table>
<tr>
<td>
Wybierz jedną parę fragmentów i określ, co mają ze sobą wspólnego
</td>
</tr>
</table>

**Przykładowe pary**
```
„Mały ptaszek całymi dniami starannie zbierał gałązki, liście i pióra
urządza swój nowy dom. Kiedy w końcu zadomowiła się w swoim przytulnym gniazdku, poczuła
poczucie dumy i zadowolenia, wiedząc, że stworzyła bezpieczną przystań
siebie i swoje przyszłe pisklęta”.

„Mały ptaszek próbował nieść gałązkę, która była dla niej za duża, a ona
skończyło się upadkiem do tyłu, nogi sterczały w powietrzu. Jej pierzastych przyjaciół
tweetował ze śmiechem, a mały ptaszek dołączył, wiedząc o tym czasami
nawet najlepiej ułożony plan może się nie udać”.
```
```
„Mały kotek chłeptał mleko swoim malutkim różowym języczkiem, robiąc słodkie minki
syczący dźwięk. Jej puszysta twarz była pokryta białymi wąsami i pozwoliła
wydając cichy pomruk zadowolenia, gdy skończyła posiłek."

„Mały kotek skubał smakołyk, delektując się każdym kęsem pyszności
smak. Jej duże, okrągłe oczy rozszerzyły się z zachwytu i zamruczała z zadowoleniem:
wdzięczny za prostą przyjemność pyszną przekąskę.”
```
```
„Szczeniak kręcił się w kółko, próbując złapać się za ogon, ale ostatecznie się przewrócił
raz po raz. Jego wybryki rozśmieszyły jego właścicieli, a nawet innych
psy w parku zatrzymały się, żeby popatrzeć na ten głupi widok”.

"Pies gonił za piłką, machając z podniecenia ogonem. Jego właściciel
rzucał piłkę raz po raz, a pies za każdym razem z radością ją aportował,
szczekanie z radości”.
```
```
„Niegrzeczny osioł pchnął nosem bramę i wbiegł do środka
łąka, rycząc z zachwytu. Jego właściciel potrząsnął głową z rozbawieniem, wiedząc
że figlarny osioł zawsze znajduje sposób na wywołanie uśmiechu na jego twarzy”.

„Złośliwy osioł gonił motyla, ale skończył
rycząc w alarmie, gdy przeleciał zbyt blisko jego twarzy. Zatoczył się do tyłu i
potknął się o własne kopyta, wywołując kilka chichotów pobliskich kurczaków”.
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#7-compare)

<p>&nbsp;</p>


## 8. Wyszukaj w tekście
**Cel** 
<table>
<tr>
<td>
Znajdź stronę, która zawiera poszukiwany tekst
</td>
</tr>
</table>

**Strony do przeszukania**
```
Strona 1: „Ptaszek ćwierkał, zbierając w dziobie gałązki i kawałki mchu, przelatując między drzewami”.
Strona 2: „Z każdą podróżą jej gniazdo nabierało kształtu, stając się bardziej przytulne i zachęcające”.
Strona 3: „I wkrótce stworzyła przytulny dom, w którym wychowała swoje lęgowe ćwierkające pisklęta”.
```
**Przykładowe frazy do wyszukania**
```
przytulniej
mały
wystarczająco
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#8-text-search)

<p>&nbsp;</p>


## 9. Klasyfikacja
**Cel** 
<table>
<tr>
<td>
Wykrywaj intencje użytkowników chatbota
</td>
</tr>
</table>

**Przykłady klas**<br/>
[Przykładowe źródło danych](https://github.com/spackows/CASCON-2017_Analyzing_chat/blob/master/sample-data/sample-NLC-training-data.csv)

Klasa: "cześć"
```
Cześć
Hej
Dobry wieczór
Dzień dobry
cześć dzień dobry
```
Klasa: "pytanie"
```
Cześć, chciałem wiedzieć, jak wyeksportować dane z notatników Pythona?
Cześć, czy mogę odzyskać usunięty notatnik?
Cześć, jak dodać folder plików do projektu?
Cześć drużyno Jak zmienić nazwę notebooka?
Jak przesłać zestaw danych z lokalnego do RStudio
Dzień dobry, czy możesz mi pomóc przesłać plik kształtu?
Jak zacząć tworzyć notatnik R?
```
Klasa: "problem"
```
Cześć, nie mogę się dzisiaj zalogować z powodu tego błędu. Konto właściciela jest nieaktywne. Może to być spowodowane wygaśnięciem członkostwa.
Nie mogę zarejestrować swojego konta, proszę o pomoc
Cześć, dostałem wiadomość, że nie udało się przygotować Object-Storage. Czy mógłbyś dać mi sugestię. Dziękuję.
Cześć, próbuję poprosić o nowy klucz dostępu API, ale nie wiem, jaki powinien być dla mnie identyfikator
Kiedy próbuję dodać model do dowolnego projektu, pojawia się błąd Nieautoryzowany.
```
**Dane wejściowe do testów**
```
Cześć Jest tam ktoś?
```
```
Masz problemy z konfiguracją usługi WML
```
```
Cześć zespole, jak mogę zaimportować dane do projektu?
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#9-classify)

<p>&nbsp;</p>


## 10. Detekcja anomalii
**Cel** 
<table>
<tr>
<td>
Znajdź odbiegający od standardów wpis
</td>
</tr>
</table>

**Data set**
```
1: "osioł"
2: "osioł"
3: "kot"
4: "osioł"
5: "osioł"
6: "osioł"
```

Zobacz: [Przykładowa odpowiedź](prompt-engineering-exercise-answers.md#10-anomaly-detection)

<p>&nbsp;</p>



## Uwaga
Wszystkie zdania i historie – o ptakach, szczeniakach, kociakach i osłach – zostały wygenerowane za pomocą chatGPT.

<p>&nbsp;</p>


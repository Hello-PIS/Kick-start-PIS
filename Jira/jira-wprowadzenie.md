# Jira - wprowadzenie do narzędzia
Ten wpis wprowadzi Was w narzędzie służące do zarządzania projektami od firmy Atlassian. Mowa oczywiście o Jirze.

## Spis treści
* [Czym jest Jira?](#czym-jest-jira)
* [Jak zacząć?](#jak-zacząć)
* [Integracja z narzędziami programistycznymi](#integracja-z-narzędziami-programistycznymi)
* [Na koniec ciekawostka](#na-koniec-ciekawostka)

## Czym jest Jira?
Cytując oficjalną stronę oprogramowania Jira to:
> Czołowe narzędzie do tworzenia oprogramowania dla zespołów korzystających z metodyk zwinnych.

W skrócie Jira to narzędzie do zarządzania pracą zespołu, śledzenia przebiegu procesów, oraz zadań. Dzięki niej łatwo można sprawdzić aktualne działania grupy, zrobione zadania, jak i czas, jaki na nie poświęcono. Dodatkowo w łatwy sposób zaplanujesz dalszą pracę.

## Jak zacząć?
Aby rozpocząć pracę z Jirą, należy utworzyć konto na [stronie oprogramowania](https://www.atlassian.com/pl/software/jira/free).
W darmowym planie mamy:
- obsługę do 10 użytkowników
- 2 GB pamięci
- tutoriale, dostęp do społeczności

Po zalogowaniu nadajemy nazwę witrynie, pod którą będzie hostowany nasza tablica.

![Strona startowa](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-strona.png)
Następnie odpowiadamy na pytania, które pozwolą oprogramowaniu dostosować rodzaj podpowiadanych instruktaży dotyczących strony.
Kolejnym krokiem będzie dodanie adresów e-mail członków naszego zespołu, aby mieli dostęp do utworzonej tablicy.
### Tworzenie tablicy dla zespołu
Oprogramowanie zaproponuje nam szablon projektu po odpowiedzi na kilka pytań związanych z naszym zespołem.

![Pytania na podstawie których stworzona będzie tablica](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-projekt.png)
![Tworzenie projektu](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-utworz-projekt.png)

Klucz projektu będzie składnikiem numeracji zadań w Jirze. Taki sposób numeracji pozwala na łatwą identyfikację, do jakiego zespołu przypisane jest zadanie.
Po początkowej konfiguracji naszym oczom ukaże się miejsce na naszą tablicę.

![Miejsce naszego tablicy](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-pierwsze-okno.png)

Aby dokończyć konfiguracje tablicy, musimy utworzyć nowy sprint. W tym celu przechodzimy do zakładki `Backlog` znajdującej się w lewym panelu. Następnie klikami na przycisk `Utwórz sprint`. Jesteśmy gotowi do utworzenia pierwszego zadania.

#### Dodatkowe funkcje
Istnieje możliwość personalizacji tablicy. Aby to zrobić, przechodzimy do zakładki `Aktywne sprinty` w lewym panelu. Następnie w lewym górnym rogu klikamy na przycisk `***` gdzie znajdziemy opcje `Ustawienia tablicy`.

Ustawienia te umożliwią nam zarządzanie kolumnami, ich nazwami, przepływami pracy, sposobami na oszacowywanie wielkości zadań czy widokiem szczegółów zgłoszeń.
### Tworzenie zadania
W górnym pasku mamy niebieski przycisk `Utwórz`. Po jego naciśnięciu zobaczymy okno, w którym będziemy mogli utworzyć nasze zadanie.

![Formularz do tworzenia zadań](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-tworzenie-zadania.png)

Utworzone zadanie znajdziemy w Backlogu, aby dodać go do aktualnego sprintu, wystarczy, że przeciągniemy je w pole z naszym sprintem.

![Utworzone zadanie](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-utworzone-zadanie.png)

#### Rodzaje zadań
W podstawowej wersji mamy dostępne 4 rodzaje zgłoszeń
| Rodzaj | Opis |
| ----------------- |--------------------:|
| Story | Przedstawia funkcje z perspektywy użytkownika. Zlecenia tego typu powinny być definiowane prostym, nietechnicznym językiem, aby były przez wszystkich rozumiane |
| Zadanie | Elementy, nie bezpośrednio związane z wymaganiami użytkownika, jednak będące koniecznymi do wykonania np. aktualizacja serwera. Zawierają bardziej szczegółowy i techniczny opis czynności do wykonania. |
| Epik | Przedstawiają istotny wynik pracy, do której zespół dąży. Grupuje historie, zadania i błędy. |
| Błąd w programie | Ułatwiają filtrowanie rzeczy koniecznych do zrobienia. Pozwalają zwrócić szczególną uwagę na błędy. |
| Pod-zadanie | Pozwala wydzielać z większego kawałku pracy mniejsze dzięki czemu, łatwiej dzielić się pracą. Stanowią bardzo szczegółowy i techniczny opis problemu. |

W ustawieniach projektu dodatkowo można zdefiniować własne typy zadania odpowiadające naszym potrzebą.

![Rodzaje zadań](https://community.atlassian.com/t5/image/serverpage/image-id/113518i7A32F598297A38B6)

### Planowanie zadań

W Jirze możemy planować dalsze działania w kolejnych sprintach. Przyda nam się do tego tworzenie między zadaniami zależności. Często bywa tak, że przed wykonaniem zadania, musimy wykonać kilka innych kroków.

![Tablica z utworzonym zadaniem](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-utworzone-zadanie.png)

Tworzenie zależności polega na połączeniu strzałką końca jednego zadania z początkiem drugiego.
### Raporty
Podczas pracy w Jirze automatycznie tworzone są raporty wizualizujące szybkość pracy zespołu, częstotliwość wdrażania rozwiązań czy też spalania zadań.

![Raporty](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-raporty.png)

### Szybki start od Jira
W Jirze dostępny jest również `Szybki start` który przeprowadzi nowych użytkowników przez podstawowe funkcje. Znaleźć go można klikając w prawym górnym rogu na ikonę naszego awatara, a następnie przechodząc do zakładki `Otwórz szybki start`.

## Integracja z narzędziami programistycznymi
Praca staje się przyjemniejsza, gdy monotonne zadania zostają zautomatyzowane. W tym rozdziale chciałabym przedstawić kilka sposobów na automatyzację pracy z Jirą.
### Integracja z repozytorium kodu na GitHubie
***
Dzięki zainstalowaniu wtyczki [Jira Software + Github](https://github.com/marketplace/jira-software-github) z łatwością można przejść z zadania w Jirze do commitów, branchy czy pull requestów.

![Wtyczka Jira Software + Github](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-github-wtyczka.png)

#### Instalacja wtyczki
Wtyczka jest w pełni darmowa, wystarczy ją zainstalować, a następnie nadać jej odpowiednie uprawnienia. Zostaniemy później przekierowani do strony konfiguracji między Jirą a Githubem. Po wypełnieniu odpowiednio danych wtyczka rozpocznie swoje działanie.

### Integracja z lokalnym repozytorium
***
Porządek w repozytorium kodu jest bardzo ważny. Dobrym pomysłem, jest nawiązywanie w commitach do numerów zadań w Jirze. W konsekwentnym podejściu do tego pomoże nam skrypt. Sprawdzi przed zapisaniem commita czy jego wiadomość zawiera numer zadania w Jirze.

![Skrypt dla lokalnego repozytorium](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-git.png)

#### Konfiguracja skryptu

Należy stworzyć skrypt `commit-msg` o treści
```sh
#!/bin/sh

export MESSAGE=$(<$1)
export JIRA_ISSUE_TAG=`HPIS-([0-9]*)`

if [[ $MESSAGE =~ $JIRA_ISSUE_TAG ]]; then
echo -e "\e[32mYes! It contains a JIRA issue! Keep it up!\e[0m"
exit 0;
fi

echo -e "\e[31mOh no... You forgot to add a JIRA issue number!\e[0m";
exit 1;
```
Następnie należy przenieść go do lokalizacji `.git/hooks/`

### Integracja z IDE
***
Podczas pracy w środowisku programistycznym firmy JetBrains przydatną może okazać się wtyczka [Jira Integration](https://plugins.jetbrains.com/plugin/11169-jira-integration). Wszystkie przypisane do Ciebie zadania, znajdziesz właśnie w tym miejscu! Dzięki temu podczas pisania kodu, w łatwy sposób możesz przypomnieć sobie treść zadania, nad którym pracujesz.

![Wtyczka Jira Integration](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-idea-wtyczka.png)

#### Instalacja wtyczki
W środowisku programistycznym po naciśnięciu `Ctrl+Shift+A` pojawi się okno, w którym należy wpisać słowo `Plugins`. Następnie zainstalować wtyczkę `Jira Integration`. Ponownie używając skrótu `Ctrl+Shift+A` i wpisać `Jira`. W lewym dolnym rogu pojawi się zakładka z taką samą nazwą. Aby przejść do dalszych konfiguracji, kliknij klucz odpowiadający opcji `Configure Server`.
Kolejny etap to dodanie naszego serwera do obsługiwanych przez wtyczkę. Po naciśnięciu `+` przechodzimy do zakładki `API Token`. Następnie uzupełniamy dane. Przykładowo:
- Server URL: `https://hello-pis.atlassian.net`
- Email: `adres_którym_logujesz_się_do_Jiry@email.com`
- API Token: Wchodzimy na stronę [Tokeny API](https://id.atlassian.com/manage-profile/security/api-tokens), klikamy `Utwórz Token API`. Wpisujemy tam etykietę, identyfikującą nasz token, a następnie kopiujemy wygenerowany token i wklejamy go do okna wtyczki.

![Konfigujracja serwera](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/config-idea.png)

Po naciśnięciu przycisku `OK` powinniśmy zobaczyć listę zadań do nas przypisanych.

## Na koniec ciekawostka
Dlaczego issue tracker od Atlassiana nazywa się Jira? Czy jest to akronim, a jeśli tak to, jak się rozwija? Jaka kryje się za tym historia?

Początkowo w firmię Atlassian do śledzenia błędów (en.: bug trackingu) służyło oprogramowanie o nazwę Bugzilla. W biurzę, programiści między sobą zaczęli nazywać je Gojira (en: Godzilla). Gdy w kolejnych latach firma zdecydowała się na stworzenie własnego narzędzia to śledzenia błędów, (w przyszłości będącego issue trackerem), nazwa tego narzędzia była oczywista. Została lekko zmodyfikowana — usunięto Go i tak powstała Jira.
Wnikliwi zapytają: ale dlaczego Gojira? Spróbujcie wykrzyczeć to na głos, jakbyście byli w trakcie bitwy! Brzmi świetnie!

## Bibliografia:
https://www.gojira.pl/2021/01/11/kurs-jira-wprowadzenie/
https://confluence.atlassian.com/pages/viewpage.action?pageId=223219957
https://www.atlassian.com/pl/software/jira
https://stackoverflow.com/questions/4870007/how-to-capture-a-git-commit-message-and-run-an-action
https://community.atlassian.com/t5/Jira-articles/Understanding-issue-types-in-jira/ba-p/1497237 

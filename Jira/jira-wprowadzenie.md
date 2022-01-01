# Jira - wprowadzenie do narzędzia
Ten wpis wprowadzi Was w narzędzie służące do zarządzania projektami od firmy Atlassian. Mowa oczywiście o Jirze. 
 
## Spis treści
* [Czym jest Jira?](#czym-jest-jira)
* [Jak zacząć?](#jak-zaczac)
* [Integracja z narzędziami programistycznymi](#integracja-z-narzedziami-programistycznymi)
* [Na koniec ciekawostka](#na-koniec-ciekawostka)


## Czym jest Jira?
Cytując oficjalną stronę oprogramowania Jira to:
> Czołowe narzędzie do tworzenia oprogramowania dla zespołów korzystających z metodyk zwinnych. 

W skrócie Jira to narzędzie do zarządznia pracą zespołu, śledzenia przebiegu procesów, oraz zadań. Dzięki niej, łatwo można sprawdzić aktualne działania grupy, zrobione zadania, jak i czas jaki na nie poświęcono. Dodatkowo w łatwy sposób zaplanujesz dalszą pracę.

## Jak zacząć?  
Aby rozpocząć pracę z Jirą należy utworzyć konto na [stronie oprogramowania](https://www.atlassian.com/pl/software/jira/free).  
W darmowym planie mamy:
- obsługę do 10 użytkowników
- 2 GB pamięci
- tutoriale, dostęp do społeczności

Po zalogowaniu nadajemy nazwę witrynie pod którą będzie hostowany nasz dashboard.  
![Strona startowa](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-strona.png)  
Następnie odpowiadamy na pytania, które pozwolą oprogramowaniu dostosować rodzaj podpowiadanych tutoriali dotyczących strony.
Kolejnym krokiem będzie dodanie adresów e-mail członków naszego zespołu, aby mieli dostęp do utworzonego dashboardu.  
### Tworzenie dashboardu dla zespołu
Oprogramowanie zaproponuje nam szablon projektu po odpowiedzi na kilka pytań związanych z naszym zespołem.  
![Pytania na podstawie których stworzony będzie dashboard](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-projekt.png)    
![Tworzenie projektu](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-utworz-projekt.png)    
Klucz projektu będzie składnikiem numeracji zadań w Jirze. Taki sposób numeracji pozwala na łatwą identyfikację, do jakiego zespołu przypisane jest zadanie. 
Po początkowej konfiguracji naszym oczom ukaże się miejsce na nasz dashboard.
![Miejsce naszego dashboardu](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-strona.png)    
### Tworzenie zadania
### Planowanie zadań
### Raporty
### Szybki start od Jira
W Jirze dostępny jest również `Szybki start` który przeprowadzi nowych użytkowników przez podstawowe funkcje. Znaleźć go można klikając w prawym górnym rogu na ikonę naszego awatara, a następnie przechodząc do zakładki `Otwórz szybki start`.

## Integracja z narzędziami programistycznymi
Praca staje się przyjemniejsza gdy monotonne zadania zostają zautomatyzowane. W tym rozdziale, chciałabym przedstawić dwa sposoby na automatyzację pracy z Jirą.
### Integracja z repozytorium kodu na GitHubie
 ***
 Dzięki zainstalowaniu wtyczki [Jira Software + Github](https://github.com/marketplace/jira-software-github) z łatwością można przejść z zadania w Jirze do commitów, branchy czy pull requestów. 

![Wtyczka Jira Software + Github](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-github-wtyczka.png)
 
 #### Instalacja wtyczki
Wtyczka jest w pełni darmowa, wystarczy ją zainstalować, a następnie nadać jej odpowiednie uprawnienia. Zostaniemy później przekierowani do strony konfiguracji między Jirą a Githubem. Po wypełnieniu odpowiednio danych, wtyczka rozpocznie swoje działanie.

### Integracja z lokalnym repozytorium
***
Porządek w repozytorium kodu jest bardzo ważny. Dobrym pomysłem, jest nawiązywanie w commitach do numerów zadań w Jirze. W konsekwentnym podejściu do tego pomoże nam skrypt. Sprawdzi przed zapisaniem commita czy jego wiadomość zawiera numer zadania w Jirze.

![Skrypt dla lokalnego repozytorium](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-git.png)
 

#### Konfiguracja skryptu

Należy stworzyć skrypt `commit-msg` o treści
```sh
#!/bin/sh

export MESSAGE=$(<$1)
export JIRA_ISSUE_TAG='HPIS-([0-9]*)'

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
Podczas pracy w środowisku programistycznym firmy JetBrains przydatną może okazać się wtyczka [Jira Integration](https://plugins.jetbrains.com/plugin/11169-jira-integration). Wszystkie przypisane do Ciebie zadania, znajdziesz właśnie w tym miejscu! Dzięki temu podczas pisania kodu, w łatwy sposób możesz przypomnieć sobie treść zadania nad którym pracujesz.

![Wtyczka Jira Integration](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-idea-wtyczka.png)

#### Instalacja wtyczki
W środowisku programistycznym po naciśnięciu `Ctrl+Shift+A` pojawi się okno, w którym należy wpisać słowo `Plugins`. Następnie zainstalować wtyczkę `Jira Integration`. Ponownie używając skrótu `Ctrl+Shift+A` i wpisać `Jira`. W lewym dolnym rogu pojawi się zakładka z taką samą nazwą. Aby przejść do dalszych konfiguracji kliknij na klucz odpowiadający opcji `Configure Server`.  
Kolejny etap to dodanie naszego serwera do obsługiwanych przez wtyczkę. Po naciśnięciu `+` przechodzimy do zakładki `API Token`. Następnie uzupełniamy dane. Przykładowo:
- Server URL: `https://hello-pis.atlassian.net`
- Email: `adres_którym_logujesz_się_do_Jiry@email.com`
- API Token: Wchodzimy na stronę [Tokeny API](https://id.atlassian.com/manage-profile/security/api-tokens), klikamy `Utwórz Token API`. Wpisujemy tam etykietę, identyfikującą nasz token, a następnie kopiujemy wygenerowany token i wklejamy go do okna wtyczki.

![Konfigujracja serwera](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/config-idea.png)

Po naciśnięciu przycisku `OK` powinniśmy zobaczyć listę zadań do nas przypisanych.

## Na koniec ciekawostka
Dlaczego issue tracker od Atlassiana nazywa się Jira? Czy jest to akronim, a jeśli tak to jak się rozwija? Jaka kryje się za tym historia? 

Początkowo w firmię Atlassian do śledzenia błędów (en.: bug trackingu) służyło oprogramowanie o nazwę Bugzilla. W biurzę, programiści między sobą zaczęli nazywać je Gojira (en: Godzilla). Gdy w kolejnych latach firma zdecydowała się na stworzenie własnego narzędzia to śledzenia błędów, (w przyszłości będącego issue trackerem), nazwa tego narzędzia była oczywista. Została lekko zmodyfikowana - usunięto Go i tak powstała Jira.   
Wnikliwi zapytają: ale dlaczego Gojira? Spróbujcie wykrzyczeć to na głos, jakbyście byli w trakcie bitwy! Brzmi świetnie!

## Bibliografia:  
https://www.gojira.pl/2021/01/11/kurs-jira-wprowadzenie/  
https://confluence.atlassian.com/pages/viewpage.action?pageId=223219957  
https://www.atlassian.com/pl/software/jira  
https://stackoverflow.com/questions/4870007/how-to-capture-a-git-commit-message-and-run-an-action

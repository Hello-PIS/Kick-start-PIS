# Jira - wprowadzenie do narzędzia
Ten wpis wprowadzi Was w narzędzie służące do zarządzania projektami od firmy Atlassian. Mowa oczywiście o Jirze. 

## Czym jest Jira?
Cytując oficjalną stronę oprogramowania Jira to:
> Czołowe narzędzie do tworzenia oprogramowania dla zespołów korzystających z metodyk zwinnych. 

W skrócie Jira to narzędzie do zarządznia pracą zespołu, śledzenia przebiegu procesów, oraz zadań. Dzięki niej, łatwo można sprawdzić aktualne działania grupy, zrobione zadania, jak i czas jaki na nie poświęcono. Dodatkowo w łatwy sposób zaplanujesz dalszą pracę.

## Jak zacząć?

### Tworzenie dashboardu dla zespołu
### Tworzenie zadania
### Planowanie zadań


## Integracja z innymi narzędziami 
Praca staje się przyjemniejsza gdy monotonne zadania zostają zautomatyzowane. W tym rozdziale, chciałabym przedstawić dwa sposoby na automatyzację pracy z Jirą.
### Integracja z repozytorium kodu



### Integracja z IDE
Podczas pracy w środowisku programistycznym firmy JetBrains przydatną może okazać się wtyczka [Jira Integration](https://plugins.jetbrains.com/plugin/11169-jira-integration). Wszystkie przypisane do Ciebie zadania, znajdziesz właśnie w tym miejscu! Dzięki temu podczas pisania kodu, w łatwy sposób możesz przypomnieć sobie treść zadania nad którym pracujesz.

![Wtyczka Jira Integration](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/jira-idea-wtyczka.png)

#### Instalacja wtyczki
W środowisku programistycznym po naciśnięciu `Ctrl+Shift+A` pojawi się okno, w którym należy wpisać słowo `Plugins`. Następnie zainstalować wtyczkę `Jira Integration`. Ponownie używając skrótu `Ctrl+Shift+A` i wpisać `Jira`. W prawym dolnym rogu pojawi się zakładka z taką samą nazwą. Aby przejść do dalszych konfiguracji kliknij na klucz odpowiadający opcji `Configure Server`.  
Kolejny etap to dodanie naszego serwera do obsługiwanych przez wtyczkę. Po naciśnięciu `+` przechodzimy do zakładki `API Token`. Następnie uzupełniamy dane. Przykładowo:
- Server URL: `https://hello-pis.atlassian.net`
- Email: adres_którym_logujesz_się_do_Jiry@email.com
- API Token: Wchodzimy na stronę [Tokeny API](https://id.atlassian.com/manage-profile/security/api-tokens), klikamy `Utwórz Token API`. Wpisujemy tam etykietę, identyfikującą nasz token, a następnie kopiujemy wygenerowany token i wklejamy go do okna wtyczki.

![Konfigujracja serwera](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Jira/photos/config-idea.png)

Po naciśnięciu przycisku `OK` powinniśmy zobaczyć listę zadań do nas przypisanych.


## Na koniec ciekawostka
Dlaczego issue tracker od Atlassiana nazywa się Jira? Czy jest to akronim, a jeśli tak to jak się rozwija? Jaka kryje się za tym historia? 

Początkowo w firmię Atlassian do śledzenia błędów (en.: bug trackingu) służyło oprogramowanie o nazwę Bugzilla. W biurzę, programiści między sobą zaczęli nazywać je Gojira (en: Godzilla). Gdy w kolejnych latach firma zdecydowała się na stworzenie własnego narzędzia to śledzenia błędów, (w przyszłości będącego issue trackerem), nazwa tego narzędzia była oczywista. Została lekko zmodyfikowana - usunięto Go i tak powstała Jira.   
Wnikliwi zapytają: ale dlaczego Gojira? Spróbujcie wykrzyczeć to na głos, jakbyście byli w trakcie bitwy! Brzmi świetnie!

Bibliografia:  
https://www.gojira.pl/2021/01/11/kurs-jira-wprowadzenie/  
https://confluence.atlassian.com/pages/viewpage.action?pageId=223219957  
https://www.atlassian.com/pl/software/jira

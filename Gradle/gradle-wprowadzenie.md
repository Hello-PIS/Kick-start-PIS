# Gradle - kick start
Poniższy artykuł poświęcony jest narzędziu służącemu do budowy projektów, czyli **Gradle**. 

## Czym w ogóle jest Gradle? 
Zgodnie z opisem podanym przez twórcę Gradle jest narzędziem do automatyzacji kompilacji do tworzenia oprogramowania w wielu językach. Opisując Gradla własnymi słowami powiedziałabym, iż jest to elastyczne narzędzie, które służy do budowy projektów. 

## Trochę teorii
Na początku spojrzymy na Gradle ze strony teoretycznej, aby zrozumieć jak to narzędzie działa w praktyce.

Gradle buduje projekt w trzech fazach:
- faza inicjalizacji,
- faza konfiguracji,
- faza wykonania.

W **fazie inicjalizacji** Gradle określa jakie projekty wchodzą w skład naszego projektu. Brzmi to jak masło maślane, jednak chodzi o to, czy projekt nasz jest prosty (składa się wyłącznie z jednego projektu) czy jest złożony (składa się z wielu podprojektów). W fazie inicjalizacji określamy więc tak naprawdę jakie podprojekty wchodzą w skład naszego projektu. Następnie dla każdego z podprojektów zostaje stworzona osobna instancja, która przechowuje konfigurację danego podprojektu. Następnie w **fazie konfiguracji** wykonywany zostaje każdy z plików konfiguracyjnych projektu. W wyniku wykonania tej fazy obiekty, które powstały w poprzedniej fazie dla każdego podprojektu, są odpowiednio konfigurowane. Na koniec w **fazie wykonania** Gradle określa zestaw wymaganych do wykonania zadań oraz ich kolejność. Zadania te zostały utworzone i skonfigurowane w poprzedniej fazie. Na końcu tej fazy Gradle wykonuje każde z zadań zgodnie z określoną kolejnością.  


## Bibliografia 
- https://docs.gradle.org/current/userguide/what_is_gradle.html


# Gradle - kick start
Poniższy artykuł poświęcony jest narzędziu służącemu do budowy projektów, czyli **Gradle**. 

## Czym w ogóle jest Gradle? 
Zgodnie z opisem podanym przez twórcę Gradle jest narzędziem do automatyzacji kompilacji do tworzenia oprogramowania w wielu językach. Opisując Gradla własnymi słowami powiedziałabym, iż jest to elastyczne narzędzie, które służy do budowy projektów. 

## Trochę teorii
Na początku spojrzymy na Gradle od strony teoretycznej, aby zrozumieć jak to narzędzie działa w praktyce.

Gradle buduje projekt w trzech fazach:
- faza inicjalizacji,
- faza konfiguracji,
- faza wykonania.

W **fazie inicjalizacji** Gradle określa jakie projekty wchodzą w skład naszego projektu. Brzmi to jak masło maślane, jednak chodzi o to, czy projekt nasz jest prosty (składa się wyłącznie z jednego projektu) czy jest złożony (składa się z wielu podprojektów). W fazie inicjalizacji określamy więc tak naprawdę jakie podprojekty wchodzą w skład naszego projektu. Następnie dla każdego z podprojektów zostaje stworzona osobna instancja, która przechowuje konfigurację danego podprojektu. Następnie w **fazie konfiguracji** wykonywany zostaje każdy z plików konfiguracyjnych projektu. W wyniku wykonania tej fazy obiekty, które powstały w poprzedniej fazie dla każdego podprojektu, są odpowiednio konfigurowane. Na koniec w **fazie wykonania** Gradle określa zestaw wymaganych do wykonania zadań oraz ich kolejność. Zadania te zostały utworzone i skonfigurowane w poprzedniej fazie. Na końcu tej fazy Gradle wykonuje każde z zadań zgodnie z określoną kolejnością.  

Gradle modeluje proces budowy jako ukierunkowany graf acykliczny (DAG) zadań. Kompilacja konfiguruje zestawy zadań i łączy je ze sobą w oparciu o ich zależność. Dzięki temu powstaje DAG. Poniżej znajdują się dwa przykładowe wykresy zadań. Wykres po lewej jest wykresem abstrakcyjnym. Oba wykresy pochodzą z oficjalnej strony Gradle. 

![Wykresy](https://github.com/Hello-PIS/Kick-start-PIS/blob/main/Gradle/photos/dag.png)

## Pierwsze kroki
W tym rozdziale opiszę od czego należy zacząć przygodę z Gradle.

### Instalacja
Jeśli nigdy wcześniej nie miałeś do czynienia z Gradlem, swoją przygodę powinieneś zacząć od jego instalacji. Jeśli chcesz tylko uruchomić istniejącą kompilację Gradle nie zawsze musisz instalować Gradle, jednak w tym poradniku skupimy się na tworzeniu własnej kompilacji. Wszelkie informacje odnośnie instalacji Gradle znajdują się na oficjalnej stronie  - [o tutaj](https://docs.gradle.org/current/userguide/installation.html).

### Budowanie aplikacji
Aby inicjować nowy projekt Gradle potrzebujemy pustego folderu, w którym znajdować będzie się nasz projekt. W pustym folderze uruchamiamy polecenie `gradle init`, które rozpocznie inicjalizację nowego projektu. W terminalu ukażą się nam pytania o kilka ustawień. Poniższa konfiguracja jest pokazana dla aplikacji w języku Kotlin.

```
Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 2

Select implementation language:
  1: C++
  2: Groovy
  3: Java
  4: Kotlin
  5: Scala
  6: Swift
Enter selection (default: Java) [1..6] 4

Split functionality across multiple subprojects?:
  1: no - only one application project
  2: yes - application and library projects
Enter selection (default: no - only one application project) [1..2] 1

Select build script DSL:
  1: Groovy
  2: Kotlin
Enter selection (default: Kotlin) [1..2] 1

Generate build using new APIs and behavior (some features may change in the next minor release)? (default: no) [yes, no]
                                                                                                                       no

Project name (default: test): kick_start
Source package (default: kick_start): kick_start

> Task :init
Get more help with your project: https://docs.gradle.org/7.3/samples/sample_building_kotlin_applications.html

BUILD SUCCESSFUL in 19m 54s
2 actionable tasks: 2 executed
```
Poniżej znajduje się struktura stworzonego przez nas projektu: 

```

├── app
|   ├── build.gradle 
│   └── src
│       ├── main
│       │   └── kotlin 
│       |           └── kick_start
│       |                  └── App.kt
│       └── test
│           └── kotlin 
│                   └── kick_start
│                          └── AppTest
├── gradle
│   └── wrapper
|       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew 
├── gradlew.bat 
└── settings.gradle 
```

Dzięki `gradle init` uzyskaliśmy konfigurację projektu, dzięki czemu możemy teraz zbudować aplikację w Kotlinie :D 

### Przejrzenie utworzonych plików
Poprzednie dwa kroki wystarczą, aby rozpocząć tworzenie aplikacji. Jeśli jednak chcemy zrozumieć, czym są, co zawierają i co robią utworzone pliki, w tym podrozdziale skupimy się właśnie na nich. 


## Bibliografia 
- https://docs.gradle.org/current/userguide/what_is_gradle.html
- https://docs.gradle.org/current/userguide/getting_started.html
- https://docs.gradle.org/current/userguide/installation.html
- https://docs.gradle.org/current/samples/sample_building_kotlin_applications.html


# Wiosna na wyspie lisów
Ten poradnik powie wam jak napisać podstawową aplikację internetową w języku Kotlin z pomocą biblioteki Spring Boot

### Spis treści
[Dlaczego Kotlin?](#dlaczego-kotlin) \
[Dlaczego Spring Boot?](#dlaczego-spring-boot) \
[Ustawienie środowiska](#ustawienie-środowiska) \
[Hello World](#hello-world) \
[Inne](#inne)

## Dlaczego Kotlin?

Kotlin to całkiem nowy język, który początkowo miał być równie bogaty w funkcjonalności co Scala, a jednocześnie kompilować i uruchamiać się znacznie od niej szybciej. Według mnie, posiada on jedną z najprostszych i najbardziej zrozumiałych składni ze wszystkich języków, nie tracąc na tym znacznie na prędkości ani stabilności napisanych programów. Dodatkowo, większość stosowanych wydań Kotlina jest oparta na JVM'ie, co ma swoje wady i zalety, ale jedną z większych zalet tego rozwiązanie jest dostęp do bogactwa bibliotek Javy, która ma ich bardzo, bardzo dużo.

## Dlaczego Spring Boot?

Spring to bibiloteka, która pozwala bardzo łatwo i szybko napisać aplikację, która po prostu działa, a jednocześnie posiada wiele przydatnych funkcjonalności.

Sam Spring jest około dwa razy starszy od Kotlina, jednak jest to jedna z nowszych i popularniejszych bibliotek dostępnych w Javie, która jest wciąż rozwijana. Posiada ona wiele wbudowanych funkcjonalności, która znacznie upraszcza chociażby tworzenie REST'owego API, łączenie z bazą danych, autentykację użytkowników, skalowalność i wiele innych.

## Ustawienie środowiska

*Uwaga! W ramach tego poradnika, zakładam że masz już zainstalowaną u siebie Javę (conajmniej w wersji 8), Gradle'a oraz podstawową znajomość Shella. Osobiście, do Kotlina i Springa polecam używać edytora IntelliJ IDEA od JetBrains, jednak rozumiem, że nie każdy może mieć do niego dostęp, dlatego w poradniku będę tworzył projekt za pomocą terminala.*

<!-- Po utworzeniu folderu w którym chcemy, aby znajdował się nas projekt i otworzeniu w nim terminala, należy wpisać w nim:

```zsh
gradle init
```

Po chwili wyświetli nam się kilka prompt'ów. W pierwszych z nich wybieramy "application", czyli w moim przypadku 2:

![gradle init](photos/gradle_init_1.png)

Następnie naturalnie wybieramy Kotlin, czyli opcję 4:

![gradle init](photos/gradle_init_2.png)

Tu wybieramy 1:

![gradle init](photos/gradle_init_3.png)

Następnie wybieramy preferowany przez nas język skryptów Gradle'a. Osobiście, polecam wziąć Kotlina, zarówno dla osób które znają Groovy'ego, jak i tych, które o nim nie słyszały.

![gradle init](photos/gradle_init_4.png)

Ostatnie dwa pytania są o nazwę projektu oraz paczki. Można podać tu dowolne nazwy, jednak radziłbym użyć jako nazwy paczki albo nazwy swojej organizacji albo nazwy projektu jak takowej nie ma, tak żeby trzymać się ze standardem.

![gradle init](photos/gradle_init_5.png)

![gradle init](photos/gradle_init_6.png)

Po tych 6 krokach Gradle utworzy nam wiele plików, z czego nas głównie będzie interesować to co znajduję się w folderze "app" -->

Najłatwiej jest zacząć projekt wchodząc na [start.spring.io](https://start.spring.io) i po lewej stronie wybrać "Gradle Project" oraz "Kotlin", po czym w polach pod Project Metadata wpisać jakąś sensowną treść, czyli nazwę aplikacji w polu Name i Artifact, nazwę swojej organizacji w Group (np. w postaci com.google) i nazwę projektu w ramach którego jest ta aplikacja tworzona (może być ona także taka sama co nazwa aplikacji). Należy także na dole strony wybrać odpowiednią wersję Javy (tzn. taką, którą ma się u siebie zainstalowaną).

![spring initializr](photos/spring_initializr_0.png)

Po tym wszytkich należy po prawej stronie wybrać guzik ADD i dodać jako zależność: Spring Web.

Po dodaniu zależności, należy wcisnąć na dole strony GENERATE, rozpakować pobrane archiwum i voilà! Mamy już gotowy początek aplikacji!

Dla sprawdzenia czy wszystko mamy poprawnie zainstalowane, możemy wejść w terminal do folderu z tym projektem i wpisać:

```zsh
gradle build
```

Po jakimś czasie, jeśli się wszystko udało, powinniśmy ujrzeć:

```zsh
BUILD SUCCESSFUL in 48s
8 actionable tasks: 8 executed
```

oraz w projekcie powinien pojawić się nowy katalog o nazwie "build"


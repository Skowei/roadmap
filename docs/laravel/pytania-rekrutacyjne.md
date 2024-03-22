---
title: "Laravel - Pytania rekrutacyjne"
---


# Pytania rekrutacyjne Laravel

1. Czym jest OOP (programowanie obiektowe)?
```
programy definiowane są za pomocą obiektów łączących atrybuty i procedury. 
Program obiektowy składa się ze zbiorów projektów komunikujących się ze sobą, w celu wykonywania konkretnych zadań.
pojęcia: hermetyzacja/enkapsulacja, polimorfizm, dziedziczenie
```

2. Jaka jest różnica między klasą abstrakcyjną a interfejsem?
```
z klasy abstrakcyjnej nie można utworzyć obiektu a może jedynie być rozszerzana przez inne klasy
inferce jest extendowany przez klasę
```

3. Jak działa sesja?
```
pozwala na przechowywanie stanu aplikacji pomiędzy zapytaniami http
```

4. Co to jest SOLID?
```
[S] Single Responsibility Principle (SRP)
    Klasa powinna mieć tylko jedną odpowiedzialność (nigdy nie powinien istnieć więcej niż jeden powód do modyfikacji klasy).

Możemy rozważyć moduł, który generuje i drukuje raport. Odpowiada on za dwa procesy, a tym samym mogą wystąpić dwa powody do jego modyfikacji. Po pierwsze, może zmienić się treść generowanego raportu, po drugie – format, w jakim jest on drukowany. Zasada pojedynczej odpowiedzialności mówi, że oba te procesy powinny być niezależne i zaimplementowane w postaci dwóch oddzielnych klas lub modułów, które komunikują się ze sobą za pomocą publicznych interfejsów. 
```
```
[O] Open/Closed Principle (OCP)
    Elementy systemu takie, jak klasy, moduły, funkcje itd. powinny być otwarte na rozszerzenie, ale zamknięte na modyfikacje[1]. Oznacza to, iż można zmienić zachowanie takiego elementu bez zmiany jego kodu. Jest to szczególnie ważne w środowisku produkcyjnym, gdzie zmiany kodu źródłowego mogą być niewskazane i powodować ryzyko wprowadzenia błędu. Program, który trzyma się tej zasady, nie wymaga zmian w kodzie, więc nie jest narażony na powyższe ryzyko. 
```
```
[L] Liskov Substitution Principle (LSP)
    Funkcje które używają wskaźników lub referencji do klas bazowych, muszą być w stanie 
    używać również obiektów klas dziedziczących po klasach bazowych, bez dokładnej znajomości tych obiektów.
```
```
[I] Interface Segregation Principle (ISP)
    Wiele dedykowanych interfejsów jest lepsze niż jeden ogólny.
```
```
[D] Dependency Inversion Principle (DIP)
    Wysokopoziomowe moduły nie powinny zależeć od modułów niskopoziomowych - zależności między nimi powinny wynikać z abstrakcji.
```

5. Opisz różnice między `$_GET` oraz `$_POST`.
```
w get odpowiedzi są ogólnodostępne i widoczne w url
w post dane nie są ogólnodostępne i są ukryte
```

6. Czym jest polimorfizm?
```
wielopostaciowość np. klasy abstrakcyjne
```

7. Co to jest PSR?
```
standardy php, mamy psr-1 oraz psr-2
```

8.  Opisz ładowanie klas w PHP.
```
przy użyciu funkcji
spl_autoload_register()
autoload() - można tylko raz i jest globalnie
```

9. Na czym polega hermetyzacja/enkapsulacja?
```
używanie public, protected, private
```

10. Jak wygląda cykl życia zapytania?
```
użytkownik ->(request) public/index.php -> autoload i instancja aplikacji -> kernel -> serviceProviders ->(dispatch Request) router
->middleware->controller->view->(response)user
```
![laravel-lifecycle](./../assets/images/laravel-lifecycle.avif)

11. CO NOWEGO W PHP 7.4
```
- funkcje strzałkowe
- array spread operator czyli $arr = [...$args]; (jak w js)
- Null coalocation czyli ?? jeżeli wartość pusta bierze drugą
- typed properties (public, protected, private zmienne)
- weak references
```

12. CO NOWEGO W PHP 8.0
```
- union types czyli deklaracja co funkcja zwraca np :void, :string, :int|float,
- JIT - czas kompilatora
- nullsafe operator czyli $arg?-> jeżeli puste to zwróci nulla i nie wywali błędu
- nazwane argumenty 🙂
- atrybuty(adnotacje)
- match czyli switch bez breaków,
- syntetyczny konstruktor czyli tworzenie zmiennych dla klasy w construct bez deklaracji.
- typ statyczny jako wartość zwracana :static
- mixed type czyli jeden z podstawowych typów zmiennych
- ::class na obiekcie - zwraca to samo co get_class()
- catch bez deklaracji zmiennej $exception, wystarczy samo \Exception
- datetime z instancji obiektu
- interfejs stringable dla wszystkiego co może używać __toString()
- str_contains - zamiennik str_post
```
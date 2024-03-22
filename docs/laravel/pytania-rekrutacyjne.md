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
infercejs jest extendowany przez klasę
```

3. Jak działa sesja?
```
pozwala na przechowywanie stanu aplikacji pomiędzy zapytaniami http
```

4. Co to jest SOLID?
```
[S] Single Responsibility Principle (SRP)
    Klasa powinna mieć tylko jedną odpowiedzialność (nigdy nie powinien istnieć więcej niż jeden powód do modyfikacji klasy).
```
```
[O] Open/Closed Principle (OCP)
    Klasy (encje) powinny być otwarte na rozszerzenia i zamknięte na modyfikacje.
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
    1. funkcje strzałkowe
        array spread operatore czyli $arr = [...$args]; (jak w js)
    2. Null coalocation czyli ?? jeżeli wartość pusta bierze drugą
    3. typed properties (public, protected, private zmienne)
    4. weak references


12. CO NOWEGO W PHP 8.0
    1. union types
    czyli deklaracja co funkcja zwraca np :void, :string, :int|float,
    2. JIT - czas kompilatora
    3. nullsafe operator czyli $arg?-> jeżeli puste to zwróci nulla i nie wywali błędu
    4. nazwane argumenty 🙂
    5. atrybuty(adnotacje)
    6. match czyli switch bez breaków,
    7. syntetyczny konstruktor czyli tworzenie zmiennych dla klasy w construct bez deklaracji.
    8. typ statyczny jako wartość zwracana :static
    9. mixed type czyli jeden z podstawowych typów zmiennych
    10. ::class na obiekcie - zwraca to samo co get_class()
    11. catch bez deklaracji zmiennej $exception, wystarczy samo \Exception
    12. datetime z instancji obiektu
    13. interfejs stringable dla wsyzstkiego co może używać __toString()
    14. str_contains - zamiennik str_post
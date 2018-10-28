---
layout: post
title:  "Pierwszy unit test w C#"
---
# powód

Powód tekstu jest dość prosty. Chciałem nauczyć się pisać testy jednostkowe z tekstów i materiałów w internecie. Poległem. Piszę więc kilka słów które może pomogą komuś kto chce zrozumieć nie tyle szczytną ideę [banalną do zrozumienia], co sposób zrobienia pierwszego testu. Bo o podstawach podstaw większość twórców poradników zapomina.
Uznaję przy tym, że piszę do kogoś takiego jak ja - kto chce zacząć, nie wie nic, a ma potrzebę.

# Pierwszy krok

Skoro tu jesteś to pewnie przeszedłeś przez w cholerę googla, YouTube, może nawet Udemy czy Courserę... i nadal jesteś zirytowany bo wiesz że chcesz testować ale ni cholery nie wiesz jak. No to co?
W czym ja to robię? Oczywiście Visual Studio Community. Bo za darmo w domu, bo zajmuje tylko kilka gb ramu [nadal mniej niż eclipse] i bo chcę w dotnety. 
Przede wszystkim podstawy o których nie ma mowy chyba w żadnych materiałach. Autorzy piszą o tym jak planować testy, jak je utrzymywać, o potrzebie, o różnych zaawansowanych rzeczach, a nie piszą o tym czym co jest.

# Gdzie te testy

Dotychczas na całkiem sporo materiałów jakie znalazłem RAZ znalazłem odpowiedź jak ogarnąć pierwszy krok. No to klikacie na swoim Rozwiązaniu/Solution w którym macie projekt który tworzycie i prawy myszy, Dodaj/Add -> NowyProjekt/NewProject -> teraz z gałęzi Test wybieracie dla .Net Framework "Projekt Testów jednostkowych (.Net Framework)", dla innych wiadomo - dopasowujesz do tego co chcesz pisać.
Teraz jak się stworzy masz w SolutionExplorer/Eksplorator Rozwiązań bogatsze drzewko, obok swojego projektu z kodem jest projekt testowy, w nim dodajesz odwołanie/Reference do projektu głównego i już twoje testy "Widzą" kod który mają testować.

# Znaczniki

Wiecie czym jest [TestClass] i [TestMethod] prawda? To znaczniki którymi poprzedzamy linię w której zaczyna się nasza klasa i nasza metoda testowa. Co ważne, a o czym wielu autorów zapomina - Odpalane w trakcie puszczenia testów jest WYWOŁANIE następującej po [TestMethod] metody, zwrotką dla wyniku testu jest wynik pozytywny lub negatywny [true or false] z Asserta występującego dalej. Metoda nie ma być booleanem i zwracać sama czegokolwiek. Nie musisz też ogarniać returna. Co jeszcze? A tak! Metody, funkcje, procedury... zwał jak zwał. Nic co jest zadeklarowane w klasie ... czy tam pliku NIE JEST wywoływane jeśli nie jest zaraz po napisie [TestMethod]. Nawet metody będące w [TestClass] nie poprzedzone [TestMethod] nie zostaną wywołane. Proste? Pewnie... teraz już tak.

# Klasy i pliki

Każdy plik .cs z projektu testowego będzie przeszukany przez VisualStudio, tam gdzie znajdzie [TestClass] będzie szukać [TestMethod] i odpali je oraz wyświetli w drzewku testów. Nie musisz ich dodatkowo linkować, podpinać, dodawać do using ani niczego... Zadziała magia silnika testów i samo się zrobi.

# Czym jest Assert do !#$$%%$^%&#$%

Autorzy piszą "po czym tworzymy asercję"... ale żaden do cholery nie mówi czym ona jest. No to po prostu... Assert to porównanie tego co zwraca nam wywołana funkcja z tym co chcemy mieć i jeśli obie strony są tym samym to test jest zdany. Np
Assert.Equal(NaszaFunkcja(JejArgumenty), true);
Jest prosto zrozumieć. Tak samo:
Assert.IsTrue(NaszaFunkcjaBooleanowska(JejArgsy));
Jest w klasie assert jeszcze trochę fajnych metod. Sprawdzających czy zwrotka jest odpowiednim typem, czy się wywaliło, czy zgłosiło wyjątek... Ale chyba sama informacja czym jest Assert jest podstawą do diaska!

# ReSharper marketing bullshit

Czas na największy bullshit jaki spotkałem ostatnio na YT - rzekomo bez ReSharpera [płatny addin] nie da się testować tylko tego co chcemy i zawsze trzeba odpalać w VS wszystkie testy, co wiadomo - przy bardziej rozbudowanym projekcie zajmie w cholerę czasu. To brednia. 
Po pierwsze. Control i klikanie myszką w wybrane testy, a potem "odpal zaznaczone". Tak to tak proste.
Po drugie. Zaznaczasz test, prawym myszki i "dodaj do listy odtwarzania" ... i masz swoją playlistę testów... możesz ich mieć milion.
Po trzecie. Możesz odpalić całą klasę testów.

# Fin!

Oczywiście polecam większość materiałów z internetów. Sam zaś nie jestem żadnym guru, majstrem ani nawet dobrym w te klocki. Zebrałem jedynie to z czym sam spotkałem się w ostatni... nie zaraz. Ja zebrałem to z czym się nie spotkałem. Z podstawami podstaw. Takimi dla samouków programowania, którzy nie mają skąd wziąć tych najważniejszych informacji - jak zrobić pierwszy krok. Bo w większości IT kroki od drugiego do tysięcznego można zrobić bez problemu używając Google i chcąc. Problem jest z pierwszym. Wszak żaden ewangelista od testów nie wpadnie na to, że najtrudniejszym jest napisać pierwszy test i zrozumieć jak to zrobić. Bo powody dlaczego... są tak oczywiste, że aż strach. Tak samo w zrozumieniu kontroli wersji nie trudno pojąć "po co", ale strasznie ciężko zrozumieć jak skonfigurować swoje konto GH, swoje środowisko... by nie psuć sobie kodu i by mądrze użyć pierwszej poza MASTER gałęzi. Bo jak zrobić drugą już każdy wie, ale jak tą pierwszą... ITD
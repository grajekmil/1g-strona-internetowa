# Strona WWW na lekcje informatyki
## Twórcy:
Filip Szostak-Sobalski\
Hanna Tylka\
Michał Szczerba
## Temat strony
cos coscos cos cos cos cos cos cos cos cos cos \
cos cos cos cos cos cos cos cos cos cos cos cos \
cos cos cos cos cos cos cos cos cos cos cos cos \
cos cos cos cos cos cos cos cos cos cos cos cos  

# Jak korzystać z Git'a - Podstawy

## Wprowadzenie

Git jest systemem kontroli wersji, który umożliwia śledzenie zmian w kodzie źródłowym projektu. Jest to bardzo przydatne narzędzie dla programistów do zarządzania kodem, współpracy z innymi programistami i śledzenia historii zmian. Poniżej znajdziesz podstawowe instrukcje dotyczące korzystania z Git'a.

## Instalacja Git'a

Najpierw musisz zainstalować Git'a na swoim systemie. Możesz to zrobić, pobierając odpowiednią wersję dla swojego systemu operacyjnego ze strony [Git Downloads](https://git-scm.com/downloads) i postępując zgodnie z instrukcjami instalacji dla danego systemu.

## Konfiguracja Git'a

Po zainstalowaniu Git'a, musisz skonfigurować swoje dane użytkownika, aby Twoje zmiany były prawidłowo oznaczane. Możesz to zrobić za pomocą poleceń:
```
git config --global user.name "Twoje Imię Nazwisko"

git config --global user.email "twoj@email.com"
```
## Inicjowanie nowego repozytorium

Aby rozpocząć nowy projekt z użyciem Git'a, musisz zainicjować nowe repozytorium. Możesz to zrobić w katalogu swojego projektu za pomocą polecenia:
```
git init
```

## Tworzenie i korzystanie z branchów

Branch w Git'cie to odgałęzienie od głównej gałęzi projektu. Jest używany do rozwijania funkcji, eksperymentowania lub izolowania prac. Aby utworzyć nowy branch, użyj polecenia:
~~~
git checkout -b nazwa_brancha
~~~

Możesz także przełączyć się na istniejący branch za pomocą:
~~~
git checkout nazwa_brancha
~~~

## Dodawanie plików do repozytorium

Kiedy masz gotowy plik, który chcesz dodać do swojego repozytorium, użyj polecenia `git add`, aby dodać go do śledzenia przez Git'a. Na przykład:
```
git add nazwa_pliku.txt
```
Możesz także dodać wszystkie pliki za pomocą:
```
git add .
```

## Zatwierdzanie zmian

Po dodaniu plików do śledzenia, musisz zatwierdzić zmiany za pomocą polecenia `git commit`. Jest to ważny krok, ponieważ tworzy on nowy punkt kontrolny w historii Twojego repozytorium. Użyj polecenia w następujący sposób:
~~~
git commit -m "Krótki opis wprowadzonych zmian"
~~~
## Untrackowanie plików

Czasami może się zdarzyć, że chcesz przestać śledzić zmiany w określonych plikach lub całych katalogach, ale nie chcesz ich usunąć z systemu plików. Może to być przydatne, na przykład gdy chcesz przestać śledzić pliki konfiguracyjne, które różnią się między środowiskami (np. lokalnym i produkcyjnym).

Aby przestać śledzić określone pliki, możesz użyć polecenia `git rm --cached`. Na przykład, jeśli chcesz przestać śledzić plik o nazwie `plik_do_untrackowania.txt`, wykonaj następujące polecenie:
~~~
git rm --cached plik_do_untrackowania.txt
~~~

Po wykonaniu tego polecenia plik zostanie usunięty z indeksu Git'a, ale pozostanie nienaruszony w systemie plików.

Jeśli chcesz przestać śledzić cały katalog, możesz to zrobić podobnie, dodając do polecenia flagę `-r` (rekursywnie):
~~~
git rm -r --cached katalog_do_untrackowania/
~~~

Po wykonaniu tego polecenia cały katalog (oraz jego zawartość) zostanie usunięty z indeksu Git'a.

Pamiętaj, że używając tych poleceń, pliki nadal będą istnieć w systemie plików, ale nie będą śledzone przez Git'a. Jeśli chcesz trwale usunąć pliki, użyj polecenia `git rm` bez flagi `--cached`.

## Wysyłanie zmian na zdalne repozytorium

Jeśli chcesz udostępnić swoje zmiany innym programistom lub przechowywać je w zdalnym repozytorium (na przykład na GitHubie), możesz wysłać je za pomocą polecenia `git push`. Przed wysłaniem zmian musisz jednak połączyć swoje lokalne repozytorium z odpowiednim zdalnym repozytorium. Możesz to zrobić używając polecenia:
~~~
git remote add origin adres_repozytorium
~~~

Gdzie `adres_repozytorium` to adres URL Twojego zdalnego repozytorium.

Po połączeniu możesz wysłać swoje zmiany na zdalne repozytorium za pomocą:
~~~
git push -u origin master
~~~

## Pobieranie zmian ze zdalnego repozytorium

Jeśli inni programiści wprowadzają zmiany do zdalnego repozytorium, możesz je pobrać do swojego lokalnego repozytorium za pomocą polecenia `git pull`:
~~~
git pull origin master
~~~

To spowoduje pobranie zmian z gałęzi `master` (głównej) zdalnego repozytorium i złączenie ich z Twoją lokalną wersją.

## Podsumowanie

To są podstawowe instrukcje dotyczące korzystania z Git'a. Pamiętaj, że Git to bardzo potężne narzędzie, które oferuje wiele innych funkcji, takich jak tworzenie i łączenie gałęzi, cofanie zmian, rozwiązywanie konfliktów, itp. Możesz zgłębić te zagadnienia w miarę jak zdobywasz więcej doświadczenia z Git'em.

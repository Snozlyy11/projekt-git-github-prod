# Konfiguracja Gita

Po zainstalowaniu Gita kolejnym krokiem jest jego konfiguracja. Ustawiamy tutaj dane użytkownika, które będą przypisane do commitów, oraz możemy przygotować połączenie z kontem GitHub.

## Ustawienie danych użytkownika

Każdy commit musi zawierać informacje, kto go wykonał. Dlatego konieczne jest podanie swojego imienia i adresu e-mail:

```bash
git config --global user.name "twoja nazwa użytkownika"
git config --global user.email "twojemail@example.com"
```

??? note "Dlaczego --global?"

    --global — oznacza, że ta konfiguracja obowiązuje dla wszystkich repozytoriów na Twoim komputerze.

## Sprawdzenie konfiguracji

Za pomocą poniższe komentyu możeszy sprawdzić naszą aktualną konfigurację.

```bash
git config --list
```
???info "Co widzisz?"

    Powinieneś zobaczyć coś takiego:
    ```bash
    user.name=twoja nazwa użytkownika
    user.email=twoj.email@example.com
    ```
## Tworzenie własnego repozytorium lokalnego

Będziemy teraz pracować cały czas w bash'u. Przećwiczymy parę kluczowych komend w terminalu.

### Pierwszy krok to utworzenie folderu dla naszego **lokalnego repo**

```bash
mkdir nasz-projekt
cd nasz-projekt
```

???question "Co jeśli nie wiemy gdzie się znajdujemy?"
    
    Jeśli mamy problem z odnaleziem się w plikach, z pomocą przychodzi nam komenda "ls" wyświelta ona drzewo plików w aktualnie znajdującym się folderze.

### Krok drugi to inicjalizacja repozytorium

```bash
git init
```

???note "Co robi git init?"
    Utworzy to ukryty folder .git, który śledzi zmiany w naszym repozytorium.

### Krok trzeci, dodajemy plik (np. test.txt)

```bash
touch plik.txt
git add .
git commit -m "Inicjalny commit"
```

???note "Rozpiska poszczególnych komend"
    **touch plik.txt** -> Tworzy pusty plik plik.txt w bieżącym katalogu.
    **git add .** -> Kropka (.) oznacza „dodaj wszystko, co zmienione w tym katalogu i podkatalogach”.
    **git commit -m "Inicjalny commit"** -> Tworzysz zapis w historii repozytorium z wiadomością "Inicjalny commit".


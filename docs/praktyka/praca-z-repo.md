# Praca z repozytorium — Podstawowe operacje

W tej części nauczysz się podstawowych komend Git używanych podczas codziennej pracy z repozytorium lokalnym i zdalnym.
Wcześniej przerabialiśmy trywialny przykład. Czas na podstawę.

---

## Sprawdzenie statusu repozytorium

```bash
git status
```

## Dodanie plików do obszaru staged

### Dodanie konkretnego pliku

```bash
git add nazwa_pliku
```

### Dodanie wszystkich zmienionych plików

```bash
git add .
```

## Tworzenie commita

Commit z wiadomością opisującą zmiany:

```bash
git commit -m "Opis zmian"
```

???note "Co to robi"
    To zapisuje zmiany w historii repozytorium lokalnego.

## Pobieranie zmian z repozytorium zdalnego
Pobierz zmiany z brancha main na GitHub:

```bash
git pull origin main
```

???note "Co robi git pull?"
    git pull pobiera zmiany z GitHub i od razu próbuje je połączyć z lokalnymi.

## Wysyłanie zmian na GitHub

```bash
git push origin main
```

???info "Przypomnijmy se co tu wykonujemy"
    Wysyłasz commit(y) na GitHub.

## Praca z branchami (gałęziami)

Wyświetlmy aktualną listę dostępnych dla nas branch'y

```bash
git branch
```

Teraz utwórzmy i przejdźmy na nowo utworzony branch

```bash
git checkout -b nazwa-brancha
```

Nadszeł czas, aby poznać składnię komendy przełączający się na istniejącego brancha

```bash
git checkout main
```

Teraz spróbujmy wypchnąć nowo utworzonego branch'a do repozytorium zdalnego na Github..

```bash
git push -u origin nazwa-brancha
```

## Scalanie branchy (merge)

Nadszedł czas na coś bardziej skomplikowanego, czyli scalanie branch'y. Jest to trudniejszy etap naszego kursu, ale spokojnie z damy sobię z tym radę.

### Scalanie z merge

Scalmy branch z **feature** do **main**:

```bash
git checkout main
git merge feature/nazwa-funkcji
```

???info "merge"
    **merge** łączy zmiany z jednej gałęzi do drugiej.

### Scalanie z rebase
Rebase (przepisanie historii):

```bash
git checkout main
git rebase feature/nazwa-funkcji
```

???warning
    Historia wygląda na bardziej liniową, ale wymaga ostrożności.

## Cofanie commitów

### --soft

```bash
git reset --soft HEAD~1
```

???note "Co robi --soft?"
    Cofa ostatni commit. Zachowuje zmiany w plikach — wracają do stanu „staged” (czyli jak po git add).

### --hard

```bash
git reset --hard HEAD~1
```

???note "Co robi --hard?"
    Cofa ostatni commit. Usuwa całkowicie zmiany w plikach. Przywraca stan repozytorium do takiego, jaki był przed tym commitem.

## Przegląd historii commitów

### Zobacz pełną historię commitów:

```bash
git log
```

### Historia w jednym wierszu 

```bash
git log --oneline
```

## Co już umiemy? 

✔️ Sprawdzić status repozytorium.

✔️ Dodawać pliki i tworzyć commity.

✔️ Pracować z branchami — tworzyć, przełączać się, scalać.

✔️ Pushować i pullować zmiany z GitHub.

✔️ Sprawdzać historię zmian.

✔️ Cofnąć zmiany, jeśli to potrzebne.
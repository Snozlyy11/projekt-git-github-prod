# 👥 Modele pracy zespołowej z Git

W pracy zespołowej z Git można korzystać z różnych modeli (workflow), które określają, jak współpracujemy nad kodem.

---

## Feature Branch Workflow (Najczęściej stosowany)

 ### Na czym polega?

- Każda nowa funkcjonalność, poprawka lub zadanie ma osobnego brancha.
- Branch jest tworzony z `main`.
- Po zakończeniu pracy tworzy się Pull Request do `main`.
- Po review — merge.

### Zalety
- Bezpieczne dla `main`.
- Łatwe śledzenie zmian i powiązanie z zadaniami.

---

## GitHub Flow

Bardzo prosty, najczęściej używany w GitHub.

- Zawsze pracujemy z `main` jako działającą wersją.
- Tworzymy krótkożyjącego brancha (`feature/xyz`).
- Wypychamy brancha na GitHub.
- Robimy Pull Request.
- Po review — merge do `main` → natychmiastowa możliwość wdrożenia (deploy).

### Zalety
- Szybkość.
- Prosta i przejrzysta historia.
- Idealny dla Continuous Deployment.

---

##  Git Flow (bardziej rozbudowany)

### Struktura

- **`main`** — wersja produkcyjna.
- **`develop`** — wersja rozwojowa.
- **`feature/*`** — nowe funkcje.
- **`release/*`** — przygotowanie do wydania.
- **`hotfix/*`** — szybkie poprawki błędów w `main`.

### Zalety
- Bardzo uporządkowana praca nad dużymi projektami.
- Wyraźne rozróżnienie etapów rozwoju.

### Wady
- Dużo branchy.
- Złożony proces — niekoniecznie dla małych zespołów.

---

## Forking Workflow (często w open source)

 Na czym polega?

- Każdy ma własne repozytorium (fork).
- Klonuje swój fork, pracuje na branchach.
- Wysyła Pull Request do głównego repozytorium (upstream).

### Zalety
- Bezpieczne — nikt nie ma dostępu do głównego repozytorium.
- Idealne dla projektów open source.

---

## Podsumowanie — który wybrać?

| Workflow               | Dla kogo?                                |
|------------------------|-------------------------------------------|
| **Feature Branch**      | Małe i średnie zespoły, codzienna praca. |
| **GitHub Flow**         | Szybkie zespoły, dev + deploy non stop.  |
| **Git Flow**            | Duże projekty, bardziej formalne procesy.|
| **Forking Workflow**    | Open source, współpraca zewnętrzna.      |

---
Jak Zacząć? Praktyczny Przewodnik


Krok 1: Instalacja Git

- Pobierz Git: Odwiedź oficjalną stronę Gita: https://git-scm.com/downloads i pobierz 
  odpowiednią wersję dla twojego systemu operacyjnego.

- Zainstaluj Git: Postępuj zgodnie z instrukcjami instalacji. W większości przypadków możesz 
  po prostu klikać "Dalej".


Krok 2: Konfiguracja Git

Po instalacji, otwórz terminal (lub Git Bash w systemie Windows) i skonfiguruj swoje dane 
użytkownika. Będą one widoczne w historii twoich commitów.


| Bash 

    git config --global user.name "Twoje Imię i Nazwisko"    
|--  
    git config --global user.email "twój.email@example.com"       


Krok 3: Tworzenie Repozytorium (Lokalnie)

Stwórz nowy folder projektu:

| Bash       
| mkdir moj-projekt-git  
|--   
| cd moj-projekt-git  


Zainicjuj repozytorium Git w tym folderze:

| Bash        
| git init  
|--

To tworzy ukryty folder .git, który przechowuje całą historię twojego repozytorium.

Krok 4: Dodawanie Plików i Commitowanie Zmian

Stwórz plik w swoim projekcie:

| Bash     
| echo "Witaj w moim pierwszym projekcie Git!" > index.html 
|--   

Dodaj plik do obszaru przechowalni (staging area):

| Bash  
| git add index.html  
|--   

Obszar przechowalni to miejsce, gdzie tymczasowo umieszczasz pliki, które chcesz 
dołączyć do następnego commita. Możesz dodać wszystkie pliki naraz używając git add .

Zatwierdź (commit) zmiany:

| Bash     
| git commit -m "Pierwszy commit: Dodano plik index.html" 
|--   

Flaga -m pozwala na dodanie krótkiej wiadomości opisującej commit. Zawsze staraj się 
pisać zrozumiałe wiadomości commitów!


Krok 5: Praca z Gałęziami (Branches)

Sprawdź, na której gałęzi jesteś:

| Bash       
| git branch 
|--   

Domyślnie będziesz na gałęzi master (lub main).

Stwórz nową gałąź:

| Bash        
| git branch nowa-funkcja 
|--   

Przełącz się na nową gałąź:

| Bash        
| git checkout nowa-funkcja
|--    

Teraz możesz bezpiecznie wprowadzać zmiany, nie wpływając na główną gałąź.

Wprowadź zmiany i zatwierdź je na nowej gałęzi:

| Bash       
| echo "To jest nowa funkcja." >> nowa-funkcja.txt  
|--  
| git add nowa-funkcja.txt    
| git commit -m "Dodano plik z nową funkcją"  
 

Wróć na gałąź główną:

| Bash       
| git checkout master  
|--  

Scal zmiany z "nowa-funkcja" do "master":
 
| Bash  
| git merge nowa-funkcja  
|--  

Git spróbuje połączyć zmiany. Jeśli wystąpią konflikty (np. dwie osoby zmieniły tę samą linię 
kodu), będziesz musiał je rozwiązać ręcznie.

Krok 6: Praca z GitHubem (Zdalne Repozytoria)

Utwórz konto na GitHubie: Jeśli jeszcze go nie masz, wejdź na https://github.com/ i załóż 
konto.

Utwórz nowe repozytorium na GitHubie:

- Po zalogowaniu, kliknij "+" w prawym górnym rogu i wybierz "New repository".

- Nadaj nazwę (np. moj-pierwszy-projekt-git).

- Możesz dodać opis, wybrać publiczne lub prywatne.

- Nie zaznaczaj opcji "Initialize this repository with a README", ponieważ już masz 
  lokalne repozytorium.

- Kliknij "Create repository".

Połącz swoje lokalne repozytorium ze zdalnym:
Po utworzeniu repozytorium na GitHubie, zobaczysz instrukcje, jak połączyć istniejące 
lokalne repozytorium. Będą wyglądać mniej więcej tak:

| Bash   
| git remote add origin https://github.com/TwojaNazwaUzytkownika/moj-pierwszy-projekt-git.git  
|--   
| git branch -M main # Zmień master na main, jeśli jeszcze tego nie zrobiłeś  
| git push -u origin main  


- git remote add origin ... : Dodaje zdalne repozytorium pod nazwą origin.

- git branch -M main: Zmienia nazwę domyślnej gałęzi na main (obecnie standard, 
  zamiast master).

- git push -u origin main: Wysyła wszystkie twoje commity z lokalnej gałęzi main 
  do zdalnego repozytorium origin na gałąź main. -u ustawia origin main jako 
  domyślne dla twojej lokalnej gałęzi, więc w przyszłości wystarczy git push.

Pobieranie zmian z GitHuba (pull):

Jeśli ktoś inny wprowadził zmiany do repozytorium na GitHubie, możesz je pobrać na swój 
lokalny komputer:

| Bash     
| git pull origin main  
|--  


Ważne Wskazówki

- Częste Commity: Robienie małych, częstych commitów z jasnymi wiadomościami ułatwia 
  śledzenie zmian i rozwiązywanie problemów.

- Gałęzie dla Nowych Funkcji: Zawsze twórz nową gałąź dla każdej nowej funkcji lub 
  poprawki błędu. To pozwala na niezależną pracę i łatwe zarządzanie wersjami.

- Pull Requesty (GitHub): Na GitHubie możesz tworzyć Pull Requesty (PR) – to sposób na 
  zaproponowanie swoich zmian do głównej gałęzi projektu. Inni programiści mogą 
  przeglądać twój kod, komentować go i zatwierdzać.

- Plik .gitignore: Twórz plik .gitignore w swoim repozytorium, aby Git ignorował pliki, 
  których nie chcesz śledzić (np. pliki konfiguracyjne, tymczasowe, zależności biblioteczne).
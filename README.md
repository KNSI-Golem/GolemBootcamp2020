
# Golem AI Bootcamp

W tym repozytorium znajdują się materiały do bootcampu z 2020 roku.

## Materiały ze spotkań

Linki z opisami:
- [Prezentacja z 3 spotkania](https://docs.google.com/presentation/d/1JlRDpKppH4yswMeG5I0UBPsca26Co5qiogMiz5_iWjA/edit?usp=sharing)
- [Prezentacja z 4 spotkania RNN](https://docs.google.com/presentation/d/1CVEP1o47k8Hc6GHKynLQqSUx_2j1CU8UMCIQhiJ95tQ/edit?usp=sharing)
## Przygotowanie środowiska do pracy

Aby przygotować środowisko do pracy z materiałami zawartymi w tym repozytorium, należy wykonać następujące kroki:

- zainstalować pythona w dowolnej wersji 3.8.x;
- zainstalować narzędzie virtualenv;
- sklonować repozytorium z materiałami;
- utworzyć środowisko wirtualne;
- zainstalować kernel jupytera korzystający z utworzonego środowiska;
- zainstalować biblioteki, które będą wykorzystywane na warsztatach;
- zainstalować jupyter notebook;


### Instalacja pythona 3.6.x

Tutaj sposób instalacji będzie zależał od systemu operacyjnego, generalnie pod tym linkiem można się dowiedzieć jak zainstalować pythona na swojej maszynie ⇒ https://www.python.org/  
**Uwaga:** Python powinien być pobrany w odpowiedniej wersji (3.6.x) oraz razem z pythonem należy zainstalować pip, czyli menadżer pakietów pythona.

Aby sprawdzić czy python i pip zostały poprawnie zainstalowane należy wpisać w konsolę komendy:
```python --version``` oraz ```pip --version```.
Output powinien wyglądać tak:
```
> python --version
Python 3.8.x
> pip --version
pip x.x.x from ... (python 3.8)
```

### Instalacja virtualenva

Należy wpisać komendę:
```
pip install virtualenv
```
Sprawdzenie:
```
> virtualenv --version
x.x.x
```

### Klonowanie repozytorium z materiałami

Należy zainstalować gita ⇒ https://git-scm.com/downloads
Można również się wesprzeć jakimś GUI, np. gitkraken, sourcetree, itp.

Po instalacji należy sklonować repozytorium spod adresu: *https://github.com/KNSI-Golem/GolemBootcamp2020.git*

W konsoli będzie to wyglądać tak:
```
> git clone https://github.com/KNSI-Golem/GolemBootcamp2020.git
```

**Uwaga:** Jeżeli do tej pory nie używałeś gita, polecam zrobić sobie kilka pierwszych kroków w tutorialu ⇒ https://learngitbranching.js.org/

### Utworzyć środowisko wirtualne

W katalogu, który powstał w wyniku wykonania poprzedniego punktu należy wykonać komendę:
```
> python -m venv projectname
```
gdzie za projectname można wstawić nazwę projektu.

Aby sprawdzić czy środowisko wirtualne działa, należy aktywować je poleceniem:
Linux:
```
> source projectname/bin/activate
```
lub
Windows:
```
> .\projectname\Scripts\activate
```

W wyniku aktywacji przed znakiem zachęty w konsoli powinna pojawić się nazwa venva:
```
(projectname) >
```

### Instalacja kernela dla utworzonego środowiska

Przy aktywowanym środowisku należy wywołać komendy:
```
(projectname) > pip install ipykernel
(projectname) > ipython kernel install --user --name=projectname
```
Po tej operacji zostanie utworzony kernel jupytera dla środowiska wirtualnego.

### Instalacja potrzebnych bibliotek

W głównym katalogu repozytorium znajduje się plik `requirements.txt`. Zawiera on wszystkie potrzebne do przeprowadzenia warsztatów biblioteki. Aby je zainstalować nalezy wywołać komendę:
```
(projectname) > pip install -r requirements.txt
```

## Sprawdzenie czy konfiguracja środowiska przebiegła pomyślnie
Należy wywołać komendę w głównym katalogu repozytorium:
```
(projectname) > jupyter notebook
```
Następnie w nowo otwartej karcie przeglądarki wybrać plik `test-environment.ipynb`.  
W nowo otwartej karcie nacisnąć przycisk run lub skrót `Ctrl+Enter`, jeżeli kod (importy) wykona się poprawnie, to znaczy, że konfiguracja przebiegła pomyślnie.

## Troubleshooting
W przypadku problemów z konfiguracją środowiska napiszcie o swoim problemie na kanale **#bootcamp** na discordzie. Zachęcamy bardziej zaawansowanych uczestników do pomagania mniej zaawansowanym. My również będziemy tam zaglądać.


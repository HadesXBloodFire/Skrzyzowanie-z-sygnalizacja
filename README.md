# Skrzyżowanie z sygnalizacją

Autor: Maciej Wilewski <br>
kontakt: mwilewski@student.agh.edu.pl

## Opis modelowanego systemu

### Opis ogólny

Model przedstawia system sterowania sygnalizacją świetlną na skrzyżowaniu z czterema wlotami. Każdy wlot jest wyposażony w:

- czujnik pojazdów,

- przycisk dla pieszych,

- sygnalizacja świetlna dla samochodów,

- sygnalizacja świetlna dla pieszych,

- buzzer dźwiękowy wspierający osoby niewidome.

System przetwarza dane z czujników i przycisków, podejmując decyzje o zmianie stanów świateł, które są przekazywane do odpowiednich urządzeń wykonawczych.

Komunikacja między komponentami odbywa się za pośrednictwem wspólnej magistrali Ethernet, a główne obliczenia realizuje procesor CPU. Pamięć oraz dwa wątki w ramach procesu kontrolera obsługują zarządzanie sensorami i sygnalizacją.

### Opis dla użytkownika

- System obsługuje realne zdarzenia z otoczenia skrzyżowania:

- Gdy czujnik wykryje pojazd, generuje odpowiedni sygnał do kontrolera.

- Naciśnięcie przycisku przez pieszego generuje żądanie przejścia.

- Kontroler analizuje dane, synchronizuje sygnalizację świetlną i wysyła nowe stany świateł do urządzeń.

- Sygnalizatory świetlne oraz buzzery dostosowują się zgodnie z poleceniem, zapewniając płynność ruchu i bezpieczeństwo pieszych.


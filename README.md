# ZADANIE 10.2.

## Punkt 2.

Dla nginx, php oraz phpmyadmin po ustawieniu replikacji ustawiam ulość kopii usług. Warto też pamiętać, że dla nginx oraz php trzeba ustawić taką samą ilość, bo nginx używa interpretera php.

Dla phpmyadmin ustawiłem jedną kopie, bo używać jej będą tylko administratorzy.

Dla mariadb mamy brak replikacji i ustawiamy uruchomienie na węźle będącym menagerem klastra.


## Punkt 3.

Skalowanie jest możliwe lda wszystkich usług bezstanowych. W tym przypadku poza mariadb będą to wszystkie usługi. Funkcjonalność swarm z Dockera nie jest polecana do replikacji baz danych ze względu na brak przystosowania tego narzędzia do takich potrzeb - tym bardziej, że bazy posiadają już swoje wewnętrzne rozwiązania replikacyjne.

## Zrzuty ekranu podczas robienia sprawozdania oraz potwierdzenie działania

![docker swarm init](/img/chmura1.png)

Tutaj wykonujemy polecenie docker swarm init.

![docker stack deploy](/img/chmura2.png)

Tutaj za pomocą docker stack deploy uruchamiam usługi.

![sprawdzenie](/img/chmura3.png)

Tutaj za pomocą polecenie docker info sprawdzam stan klastra.

![sprawdzenie](/img/chmura44.png)

Tutaj wszedłem na port 6666 aby sprawdzić, czy index.php poprawnie się wyświetla na serwowanej stronie.

![sprawdzenie](/img/chmura55.png)

Tutaj sprawdzam również działanie phpmyadmina. Mieści się on na porcie 6001.

![sprawdzenie](/img/chmura6.png)

Tutaj zalogowałem się do phpmyadmin na roota, aby sprawdzić, czy wszystko jest ok.

## PODSUMOWANIE

Udało się wszystko przeprowadzić według intrukcji i polecenia. Wszystko działa poprawnie :)
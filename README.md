# mGenerator
Zdarza się, że prosta strona internetowa (np. wizytówka) ma tylko kilka podstron. Chcielibyśmy, aby miała ich więcej, najlepiej kilka tysięcy i aby były względnie sensowne.
Poniższy skrypt jest rozwiązaniem tego problemu. Jeśli możesz w jakiś sposób powiązać stronę z miejscowościami w Polsce, skrypt pomoże Ci to zrobić.
Przy jego pomocy możesz wygenerować ok. czterech tysięcy podstron (po jednej dla każdej miejscowości), ich mapę w formacie Google, a także spingować ją do Google i Binga.

Skrypt pobiera kod strony ze strony głównej, na podstawie którego tworzysz templatkę dla tworzenia podstron.
Skrypt sam zastępuje każdą frazę kluczową w kodzie sklejką "fraza kluczowa + miejscowość".
Dodatkowo umieści nazwę miejscowości tam, gdzie umieścisz ciąg "{miasto}" i dołączy kilka linków wewnętrznych do innych podstron tam, gdzie umieścisz ciąg "{linki}". Pozwala również sformatować linki tak, aby pasowały do strony.

Można wkleić kod php (np. include dla SWL-a albo web-toolsa) i można poprawki dla kilku tysięcy podstron wprowadzać w jednym pliku.

Uwaga! kod php wklejamy na razie nietypowo, zamiast otwierającego znacznika <?php stosujemy ciąg dwóch znaków '; a zamiast zamykającego ?> stosujemy echo ' - postaram się to w przyszłości uprościć.

W efekcie otrzymujemy paczkę z podstronami, którą należy rozpakować i wgrać na serwer. Następnie uruchamiamy mały skrypt zawarty w paczce i to już wszystko.

Dla nazwa.pl trzeba zamiast:

RewriteEngine on

wrzucić:

RewriteEngine on
RewriteBase /

do pliku .htacces

Na marginesie dodam, że tak wygenerowane podstrony ładnie i dość szybko się indeksują, zwiększając site strony do rozsądnych rozmiarów.

Skrypt jest wczesną wersją, może zawierać błędy.

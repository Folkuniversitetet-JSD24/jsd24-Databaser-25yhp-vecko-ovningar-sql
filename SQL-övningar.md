SQL - övningar - DVD Rental (PostgreSQL)

Instruktioner

2a Skriv en SELECT-query som visar titlarna (title) på alla filmer i tabellen film. 

2b Resultatet ska sorteras i stigande bokstavsordning.

3 Skriv en SELECT-query som visar titlarna (title) på alla filmer där skådespelaren med actor_id = 58 medverkar.
Använd tabellerna film, film_actor och actor.

4 Skriv en SELECT-query som visar för- och efternamn (first_name, last_name) på alla kunder som bor i Kanada.

4b Sortera resultatet i stigande bokstavsordning efter efternamn (last_name).
Tips: Använd JOIN mellan tabellerna customer, address, city och country.

5 Skriv en SELECT-query som visar för- och efternamn på alla kunder som har adressen registrerad i staden 'Buenos Aires'.
Tips: Använd JOIN mellan customer, address, city.

6 Skriv en SELECT-query som visar alla kunder som saknar e-postadress (email IS NULL).
Tips: email finns i tabellen customer, och NULL-värden kan sökas med IS NULL.

7 Skriv en SELECT-query som visar för- och efternamn på alla kunder som bor i antingen Sverige eller Spanien.
Använd IN ('Sweden', 'Spain') i WHERE-satsen.

8 Skriv tre olika SELECT-queries som besvarar följande frågor:
a) Finns det några kunder i USA (country = 'United States') som INTE har någon e-postadress?
b) Finns det några kunder i USA som HAR en e-postadress?
c) Finns det några kunder i delstaten Kalifornien (district = 'California') som har e-post?
Tips: Fältet email finns i tabellen customer. district finns i tabellen address. Använd IS NULL, IS NOT NULL och JOIN.

9 Skriv en SELECT-query som visar alla e-postadresser (email) från tabellen customer som uppfyller minst ett av följande villkor:
Slutar på 'com'
Börjar med 'jack' eller 'stan'
Innehåller ordet 'murray'
Tips: Använd LIKE, OR, och %.

10a Visa för- och efternamn på alla kunder som har ett postnummer (postal_code) som börjar på '6', '7', '8' eller '9'.
Postnumret finns i tabellen address.
Tips: Använd LEFT(postal_code, 1) eller SIMILAR TO. (Behöver du göra en strängjämförelse?)

10c Visa alla kunder med postnummer enligt ovan som bor i staden 'Copenhagen'.

10d Visa alla kunder med postnummer enligt ovan som bor i antingen 'Copenhagen' eller 'Paris'.

11a Visa alla filmer (title) från tabellen film som inte har priset 0.99 i kolumnen rental_rate.

11b isa alla filmer (title) från tabellen film vars namn börjar på 'Go'

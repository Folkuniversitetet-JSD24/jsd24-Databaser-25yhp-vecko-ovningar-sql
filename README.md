# jsd24-Databaser-25yhp-vecko-ovningar-sql

Här samlar jag alla övningar ni övar på när det inte är lektion.

---
🎮 **Frivillig startövning – SQL Murder Mystery**

: https://mystery.knightlab.com/

Kommentar: Detta är ett roligt webbläsarspel där du löser ett SQL-mordmysterium genom att skriva SQL-frågor.
🧠 Spelet körs med en inbyggd SQLite-databas och fungerar **endast i webbläsaren**.  
🟢 **Du behöver inte installera något** – bara öppna länken och börja skriva SQL direkt.

📌 **OBS!** Detta är inte kopplat till PostgreSQL eller DVD Rental. Det är en separat övning som tränar din SQL-logik och felsökning.

---
Jag testade att skapa ett eget Murder Mystery men som förhoppningsvis funkar med PostgreSQL.

🎮 **PostgreSQL Murder Mystery**
: https://github.com/Folkuniversitetet-JSD24/jsd24-Databaser-25yhp-vecko-ovningar-sql/blob/main/PostgreSQLMurderMysteryPostgreSQLMurderMystery.md

FACIT (Titta här såklart efter ni försökt och eventuellt löst det eller gett upp =D ).
: https://github.com/Folkuniversitetet-JSD24/jsd24-Databaser-25yhp-vecko-ovningar-sql/blob/main/FACITPostgreSQLMurderMysteryPostgreSQLMurderMysteryFACIT.md

---

➡️ När du spelat klart, går du vidare till DVD Rental-databasen och de SQL-övningarna nedanför.

---

## 🗃️ Exempeldatabas: DVD Rental

Vi använder en färdig testdatabas för PostgreSQL kallad **DVD Rental**.

📥 **Ladda ner databasfilen (.zip):**  
https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip

---

🧑‍💻 **Instruktioner för att importera DVD Rental till PostgreSQL:**

1. Extrahera `.zip`-filen tills du har `dvdrental.tar`

2. Skapa en tom databas i pgAdmin eller med kommandot:  
Terminalen: createdb dvdrental

3. Importera databasen med följande kommando i terminalen:
Terminalen: pg_restore -U postgres -d dvdrental -1 dvdrental.tar

Byt ut postgres mot ditt användarnamn om det är ett annat.

---

SQL-övningar.md för PostgreSQL (DVD Rental): [https://gist.github.com/zocom-christoffer-wallenberg/417dfa1dc4ca5aa5046c4eb1dd31b124
](https://github.com/Folkuniversitetet-JSD24/jsd24-Databaser-25yhp-vecko-ovningar-sql/blob/main/SQL-%C3%B6vningar.md)

Tips! Använd W3Schools SQL guide för ovanstående övningar: https://www.w3schools.com/sql/

---

# jsd24-Databaser-25yhp-vecko-ovningar-sql

Här samlar jag alla övningar ni övar på när det inte är lektion.

---

Starta med detta spel: https://mystery.knightlab.com/

Fortsätt därefter med nedan övningar

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


SQL-övningar.md för PostgreSQL (DVD Rental): [https://gist.github.com/zocom-christoffer-wallenberg/417dfa1dc4ca5aa5046c4eb1dd31b124
](https://github.com/Folkuniversitetet-JSD24/jsd24-Databaser-25yhp-vecko-ovningar-sql/blob/main/SQL-%C3%B6vningar.md)

Tips! Använd W3Schools SQL guide för ovanstående övningar: https://www.w3schools.com/sql/

-------------------------




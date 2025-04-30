# 🕵️ PostgreSQL Murder Mystery – Övning

## 📚 Bakgrund
Ett mord har skett på Tech Conference 2025. Fyra misstänkta är identifierade, men bara en av dem ljuger. 
Kan du ta reda på vem mördaren är genom att analysera deras alibin, loggar och bevis?

## 🎯 Din uppgift:
Ta reda på vem som ljuger om sitt alibi och sannolikt är mördaren.

För att lyckas behöver du:
- Läsa tabellerna och förstå strukturen
- Kombinera data från flera tabeller (t.ex. `alibi`, `location_log`, `evidence`)
- Jämföra vad de säger att de gjorde – med vad loggen visar
- Fundera på *vem som var på fel plats vid fel tidpunkt*

## 🧠 Tips:
- Använd `JOIN` för att koppla samman information
- Filtrera med `WHERE`
- Se om något inte stämmer mellan tabellerna
- Använd `ORDER BY`, `!=`, `IS NULL` eller andra verktyg du lärt dig
- Du kan börja med att titta på tabellerna var för sig: `SELECT * FROM suspect;` osv.
- 💡 Bonus: Kan du skriva en query som returnerar den skyldige direkt?

---

## 🛠️ 1. SQL för att skapa tabeller och data

```sql
-- Skapa tabeller
CREATE TABLE suspect (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  occupation TEXT,
  age INT
);

CREATE TABLE alibi (
  id SERIAL PRIMARY KEY,
  suspect_id INT REFERENCES suspect(id),
  alibi_time TIMESTAMP,
  location TEXT
);

CREATE TABLE location_log (
  id SERIAL PRIMARY KEY,
  person_name TEXT,
  timestamp TIMESTAMP,
  location TEXT
);

CREATE TABLE evidence (
  id SERIAL PRIMARY KEY,
  description TEXT,
  timestamp TIMESTAMP,
  found_at TEXT
);
```

---

## ➕ 2. Fyll tabellerna med data

```sql
-- Misstänkta
INSERT INTO suspect (name, occupation, age) VALUES
  ('Alice', 'Utvecklare', 29),
  ('Bob', 'Systemadmin', 42),
  ('Charlie', 'Datasäkerhet', 37),
  ('Diana', 'Projektledare', 33);

-- Alibis
INSERT INTO alibi (suspect_id, alibi_time, location) VALUES
  (1, '2025-05-01 13:30:00', 'Lunchrestaurang'),
  (2, '2025-05-01 13:45:00', 'Kontoret'),
  (3, '2025-05-01 13:40:00', 'Datasal'),
  (4, '2025-05-01 13:30:00', 'Mötesrum');

-- Loggdata
INSERT INTO location_log (person_name, timestamp, location) VALUES
  ('Alice', '2025-05-01 13:30:00', 'Lunchrestaurang'),
  ('Bob', '2025-05-01 13:45:00', 'Datasal'), -- 😮 fel plats!
  ('Charlie', '2025-05-01 13:40:00', 'Datasal'),
  ('Diana', '2025-05-01 13:30:00', 'Mötesrum');

-- Bevis
INSERT INTO evidence (description, timestamp, found_at) VALUES
  ('Kniv med fingeravtryck', '2025-05-01 13:45:00', 'Datasal');
```

---

## 🧩 Vad du kan undersöka med SQL-frågor:

- Lista alla misstänkta
- Jämföra alibi med platslogg
- Se vem som inte befann sig där den sa sig vara
- Se var beviset hittades
- Kombinera `JOIN`, `WHERE`, `ORDER BY` m.m.

# 🕵️ PostgreSQL Murder Mystery – Facit

## ✅ Uppgift:
Ta reda på vem som ljuger om sitt alibi genom att jämföra deras påstådda plats (alibi) med vad som faktiskt finns loggat i `location_log`, samt var bevis hittades.

---

## ✅ Steg-för-steg med SQL-exempel:

### 1. Visa alla misstänkta
```sql
SELECT * FROM suspect;
```

### 2. Visa alibin för alla misstänkta
```sql
SELECT s.name, a.alibi_time, a.location
FROM suspect s
JOIN alibi a ON s.id = a.suspect_id;
```

### 3. Visa alla platsloggar
```sql
SELECT * FROM location_log;
```

### 4. Jämför om någon har en platslogg som inte matchar deras alibi
```sql
SELECT s.name, a.location AS alibi_location, l.location AS actual_location
FROM suspect s
JOIN alibi a ON s.id = a.suspect_id
JOIN location_log l ON s.name = l.person_name AND a.alibi_time = l.timestamp
WHERE a.location != l.location;
```

🎯 **Resultat:**  
Personen vars alibi inte matchar loggen är **Bob**. Han påstår sig ha varit på "Kontoret", men loggen visar att han var i **Datasal** – där även beviset hittades.

---

### 5. Visa var beviset hittades
```sql
SELECT * FROM evidence;
```

### 6. Bonus: Hämta direkt namnet på den misstänkte som ljuger
```sql
SELECT s.name
FROM suspect s
JOIN alibi a ON s.id = a.suspect_id
JOIN location_log l ON s.name = l.person_name AND a.alibi_time = l.timestamp
WHERE a.location != l.location;
```

---

🧩 **Slutsats:**
Bob är den skyldige. Hans alibi är falskt och han befann sig vid platsen där beviset hittades.

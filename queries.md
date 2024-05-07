- Basic SELECT query:
```SELECT * FROM db_name.table_name```

- Basic data exploration:
```Limiting data, Sorting in desc order, ```

* Exercises:
```sql
SELECT name FROM dvd_rentals.category ORDER BY category_id DESC LIMIT 1;
```

```sql
SELECT title, rating FROM dvd_rentals.film ORDER BY length desc, replacement_cost;
```
```sql
SELECT rating, COUNT(*) AS frequency, ROUND(100 * COUNT(*)::NUMERIC / SUM(COUNT(*)) OVER (), 2) AS percentage
FROM dvd_rentals.film_list 
GROUP BY rating
ORDER BY frequency desc;
```

> This is used to emphasize text.
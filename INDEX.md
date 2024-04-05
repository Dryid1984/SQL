REMEZOV ALEXANDR
Задание 1
Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.
![image](https://github.com/Dryid1984/SQL/assets/152690390/6bafa98a-6649-4670-9547-3f212cfab649)
Задание 2
Выполните explain analyze следующего запроса:
select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id
2.1 перечислите узкие места;
2.2 оптимизируйте запрос: внесите корректировки по использованию операторов, при необходимости добавьте индексы.
2.1
излишние таблицы inventory, rental и film
2.2
![image](https://github.com/Dryid1984/SQL/assets/152690390/2388074e-7534-47d1-9ac8-faa76b96a104)
![image](https://github.com/Dryid1984/SQL/assets/152690390/e68321ad-e910-4f2a-a366-ac8d18d9225a)


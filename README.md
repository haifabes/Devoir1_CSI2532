# Devoir1_CSI2532

B1.
1. Returns 2 columns; name with the name of users who use MS Word and their experience with the software 




2. 



B2.
a.   
```    
      SELECT name 
        FROM users
        WHERE join_date < '2020-01-01'
        
```
	

b. 
```
SELECT 
        name,
        COUNT(*) AS software_num
        FROM users i, licenses l
        WHERE 
                l.user_id=i.id
        GROUP BY i.name
        ORDER BY i.name; 
        
```
c.

```

INSERT INTO users (id, name, join_date)
VALUES
(52, 'abby', '2018-01-01'),
(53, 'zoe', '2019-01-02'),
(54, 'jack', '2020-01-02');

INSERT INTO licenses (user_id, software_name, access_code)
VALUES
(52, 'MS Word', 'agj123'),
(53, 'MS Word', 'd22545'),
(54, 'MS Word', 'hijh579'),
(52, 'Sketch', 'x15743');
```

d.
```
UPDATE softwares 
SET version='51', released_date='2020-01-01'
WHERE name ='Sketch';
```

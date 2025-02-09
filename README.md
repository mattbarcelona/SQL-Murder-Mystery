# SQL-Murder-Mystery

from https://mystery.knightlab.com/

You vaguely remember that the crime was a ​murder​ that occurred sometime on ​Jan.15, 2018​ and that it took place in ​SQL City​. Start by retrieving the corresponding crime scene report from the police department’s database.

SELECT \*
FROM sqlite_master
where type = 'table'

Response

![image](https://github.com/user-attachments/assets/c4d5b41c-bc5b-46f6-b2a8-c1756c4a0949)
![image](https://github.com/user-attachments/assets/d4d7d4cb-b5f2-45a1-bf2c-1906fd587e70)
![image](https://github.com/user-attachments/assets/5ada2d0f-2632-48e0-9896-b51d353dcc8b)

SELECT * 
FROM crime_scene_report;

Display all crimes reports

SELECT *
FROM crime_scene_report
WHERE type = "murder";

Display all murders from datatase

SELECT *
FROM crime_scene_report
WHERE type = "murder"
	AND date = "20180115"
	AND city = "SQL City";

 ![image](https://github.com/user-attachments/assets/736b815c-6d85-4403-89be-b6c664e71de3)


SELECT *
FROM person;

Display all people from database

First witness living at the last house of the road

![image](https://github.com/user-attachments/assets/8b49842a-f958-4b29-a562-2ffd320c175f)


Second witness:

SELECT *
FROM person
WHERE name LIKE '%Annabel%'
AND address_street_name = "Franklin Ave";

Interviews:
SELECT *
FROM interview
WHERE person_id IN ("14887", "16371");

![image](https://github.com/user-attachments/assets/00cd25f2-26ab-49e0-b82f-6bedbd409731)

Clues from Gym club

SELECT *
FROM get_fit_now_check_in
WHERE membership_id LIKE '48Z%'
	AND check_in_date = "20180109";

 ![image](https://github.com/user-attachments/assets/2511fc21-1501-47c1-bfa2-97eafc9cb28b)


Clue from car plate:

SELECT *
FROM drivers_license
WHERE gender = "male"
	AND plate_number LIKE '%H42W%';

 ![image](https://github.com/user-attachments/assets/0d0d0d65-2d18-43cc-9f03-044d993a94ae)

Checking License ID:

SELECT *
FROM person
WHERE license_id IN ("423327", "664760");

![image](https://github.com/user-attachments/assets/e24add61-c00f-48a6-a76b-336c2828e38c)


Checking if one of the two go to the gym:

SELECT *
FROM get_fit_now_member
WHERE person_id IN ("51739", "67318");

![image](https://github.com/user-attachments/assets/cf9c627b-c22d-448e-b36b-5143fcf0671e)

The murderers is:

![image](https://github.com/user-attachments/assets/e702346e-0c23-4215-a1ba-fc07cac452a8)


![image](https://github.com/user-attachments/assets/4c06ded8-0845-42f0-821a-ea38d9b70db5)

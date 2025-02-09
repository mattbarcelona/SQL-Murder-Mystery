# SQL-Murder-Mystery

from https://mystery.knightlab.com/

You vaguely remember that the crime was a ​murder​ that occurred sometime on ​Jan.15, 2018​ and that it took place in ​SQL City​. Start by retrieving the corresponding crime scene report from the police department’s database.

SELECT \*
FROM sqlite_master
where type = 'table'

Response

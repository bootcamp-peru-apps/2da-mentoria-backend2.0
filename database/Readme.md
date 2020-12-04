# DATABASE

## Backup
```bash
docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql
```
- example : Only dev password
```bash
docker exec enpp_db /usr/bin/mysqldump -u root --password='4DQ.<Ya9!K,63R.z' sitedb > $(date +%Y-%m-%d).sql
```

# Restore 
```bash
 cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE
```
- This auto init proyect

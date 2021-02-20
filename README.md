# school-form-import-responses
Populates the school-form database with survey responses extracted from Google Forms.

Designed as a helper to set up: [https://github.com/Marcos-A/school-form](https://github.com/Marcos-A/school-form)

---

### Requirements:
1. Install:

```
sudo apt-get install python3	
sudo apt-get install libpq-dev python-dev
sudo apt install python3-pip
pip3 install psycopg2
pip3 install pytz
```

2. Set up your "database.ini" file and place it in the project's root folder:

```
[postgresql]
host=YOUR-HOST
database=YOUR-DATABASE
user=YOUR-USER
password=YOUR-PASSWORD
port=YOUR-PORT
options=-c search_path=dbo,YOUR-SCHEMA
```

3. Your data to be imported must be in a CSV file following the pattern:

```
header: TIMESTAMP,GRUP,OBJECTE,MP-ÍTEM1,MP-ÍTEM2,MP-ÍTEM3,MP-ÍTEM4,MP-COMENTARI,TUTORIA1-ÍTEM1,TUTORIA1-ÍTEM2,TUTORIA1-ÍTEM3,TUTORIA1-COMENTARI,TUTORIA2-ÍTEM1,TUTORIA2-ÍTEM2,TUTORIA2-ÍTEM3,TUTORIA2-ÍTEM4,TUTORIA2-COMENTARI,CENTRE-ÍTEM1,CENTRE-ÍTEM2,CENTRE-ÍTEM3,CENTRE-ÍTEM4,CENTRE-ÍTEM5,CENTRE-ÍTEM6,CENTRE-COMENTARI
```


---

### How to run
From within the project's root folder, run:

`python3 insert_data.py YOUR-RESPONSES-CSV-FILE.csv`

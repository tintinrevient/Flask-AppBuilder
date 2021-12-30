# Minimal Example

## Setup

1. Use the default skeleton application, i.e., `run:app`:
```bash
export FLASK_APP=app
```

2. Create the admin user:
```bash
flask fab --create-admin
```

3. Check the default sqlite database:
```bash
sqlite3 app.db

sqlite> .table
ab_permission            ab_register_user         ab_user_role
ab_permission_view       ab_role                  ab_view_menu
ab_permission_view_role  ab_user

sqlite> select * from ab_user;
1|admin|user|admin|pbkdf2:sha256:150000$XYZi928E$92f808e4b51c2601c25d4f80c7a53fbaf19d7ea323a5ab779a5d3c430a7478c1|1|admin@fab.org|2021-12-30 13:32:53.946392|2|0|2021-12-30 13:21:00.829089|2021-12-30 13:21:00.829102||
```

4. Start the app:
```bash
python run.py
```

## References
* https://flask.palletsprojects.com/en/2.0.x/cli/

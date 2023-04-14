# YaMDb API
YaMDb API — collecting reviews of mediacontent.

## Description

Expandable and Flexible The YaMDb collects user feedback on mediacontent.

### template .env in location infra/.env
```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

### Description of commands to run an application in containers:

Clone the repository:
```bash
git clone https://github.com/zakharovvladimir/infra_sp2.git
```

Creating and activating the virtual environment:
```bash
python3 -m venv venv
source /venv/Scripts/activate
```

Set the dependencies:
```bash
pip install -r requirements.txt
```

Raising containers:
```bash
docker-compose up -d --build
```

Performing migrations:
```bash
docker-compose exec web python manage.py migrate
```

Creating a superuser:
```bash
docker-compose exec web python manage.py createsuperuser
```

Collecting statics:
```bash
docker-compose exec web python manage.py collectstatic --no-input
```

Create a database dump:
```bash
docker-compose exec web python manage.py dumpdata > fixtures.json
```

## Contributing and Contacts

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Feel free to contact: vladimir.zakharov.s@yandex.ru
github.com/zakharovvladimir

## License

[MIT](https://choosealicense.com/licenses/mit/)


![example workflow](https://github.com/github/docs/actions/workflows/main.yml/badge.svg)

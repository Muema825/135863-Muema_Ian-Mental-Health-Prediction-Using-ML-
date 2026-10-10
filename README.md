135863-Muema_Ian
Supervisor - Mr.Patrick Shabaya

Abstract
One in four people suffer from mental illnesses at one point in their lives, this is not only in
Kenya, but throughout the world according to the World Health Organization’s report. Before the pandemic hit, mental illness was regarded as a topic of controversy in public debate. After the pandemic hit, mental health was taken seriously by employees who were aware that it hampered the productivity of its employees. Many people do not seek help for mental health problems because of issues such as stigmatization, lack of access to mental health services and lack of finances to visit mental health clinics. The main aim of the project is to develop a website that will use machine learning algorithms that have been trained on a large number of mental health assessment data sets to help the users diagnose their mental health problems, overtime it will be updated to improve its accuracy. The users can anonymously complete the mental health assessments and their data will be kept confidential. The machine learning algorithms will be trained to find a specific diagnosis of mental illnesses such as depression, anxiety and bipolar disorder. The website will be an effective tool to raise awareness on mental health issues and it will have a major impact on mental health care while encouraging people to seek help when necessary.

## Configuration

Secrets are read from environment variables, not from files in the repository.
Copy `.env.example` and set the values in your shell or deployment environment
(Django does not load `.env` automatically, so export them, e.g. `set -a; . ./.env; set +a`):

| Variable | Purpose |
| --- | --- |
| `DJANGO_SECRET_KEY` | Django secret key. Required unless `DJANGO_DEBUG=True` (a dev-only fallback is used then). |
| `DJANGO_DEBUG` | `True` for local development; defaults to `False`. |
| `DJANGO_ALLOWED_HOSTS` | Comma-separated host names, e.g. `example.com,www.example.com`. |
| `DJANGO_DB_PATH` | Optional path to the SQLite database (default `db.sqlite3` in the project root). |
| `EMAIL_HOST`, `EMAIL_PORT`, `EMAIL_USE_TLS` | SMTP server settings. |
| `EMAIL_HOST_USER`, `EMAIL_HOST_PASSWORD` | SMTP login (use an app password for Gmail). |
| `GOOGLE_APPLICATION_CREDENTIALS` | Optional path to a Google service-account JSON key kept outside the repo. |

The database is not committed. Create it locally with:

```bash
python manage.py migrate
python manage.py createsuperuser   # optional, for the admin site
python manage.py runserver
```

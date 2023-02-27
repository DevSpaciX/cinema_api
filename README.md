# Cinema API
- Api service for cinema managment written on DRF

## Feauters:
- JWT authenticated
- Admin panel /admin/
- Documentation is located via /api/doc/swagger/
- Managing orders and tockets
- Media files on movie image (stored in docker )
- Creating movies with actors , genres 
- Filtering movies and movie sessions
- Docker app starts only when db is available ( custom command via management/commands )

## Installing using GitHub:
-Install Postgres and create DB

```python
git clone https://github.com/DevSpaciX/cinema_api.git
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
open .env.sample and change enviroment variables on yours !Rename file from .env.sample to .env
python manage.py migrate
python manage.py runserver
```
## Run with Docker:
- Docker should be installed

docker-compose build
docker-compose up

## Getting access:
- Create user via /api/user/register/
- Get user token via /api/user/token/
- Authorize with it on /api/doc/swagger/ OR 
- Install ModHeader extention and create Reqest header with value ```Bearer <Your access tokekn>


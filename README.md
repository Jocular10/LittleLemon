# LittleLemon (Meta Backend Developer Capstone)
## Running
Please create a `.env` file like this, or the project won't run.  
```bash
SECRET_KEY="your-secret-key"
DB_NAME="db"
DB_HOST="127.0.0.1"
DB_PORT="3306"
DB_USER="root"
DB_PASSWORD=""
```
Then, install the dependencies and apply migrations:  
```bash
pipenv install
pipenv run python3 manage.py makemigrations
pipenv run python3 manage.py migrate
```
Finally, run the server:
```bash
pipenv run python3 manage.py runserver
```
## Notes
Only authenticated users can book.  
Only superusers can see all the bookings or add menu items.
Test the following endpoints:
```bash
restaurant <- index, serving html contents
restaurant/menu <- get/post menu items through insomnia
restaurant/book <- get/post books through insomnia
```
I used `authtoken` for authentication, see the `authn/urls.py` file to check the endpoints.  
# Key Concepts — v5
 
## SQLALCHEMY_DATABASE_URI
Tells SQLAlchemy which database to connect to.
Format: dialect://user:password@host:port/dbname
Example: postgresql://postgres:secret@localhost:5433/universitydb
                                                 ^^^^
         Port 5433 = Docker host mapping to container's 5432
 
## SQLAlchemy(app)
Initialises the ORM and binds it to the Flask application.
After this, db.session and db.engine are available everywhere.
 
## db.engine.connect()
Opens a raw connection — useful only for testing.
In normal use, SQLAlchemy manages connections automatically
via the connection pool.
 
## Temporary test routes
It is good practice to add a /check route, verify it works,
then DELETE the route before committing. Never ship debug routes.
 
# From v4
## load_dotenv()         — loads .env
## os.environ.get()      — reads config safely
## .gitignore            — keeps secrets out of git

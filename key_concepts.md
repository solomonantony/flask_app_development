# Key Concepts — v4
 
## load_dotenv()
Reads .env and injects each KEY=value pair into os.environ.
Must be called before os.environ.get().
 
## os.environ.get('KEY', 'default')
Reads an environment variable. Returns the default if the key
is missing, preventing a crash on misconfigured machines.
 
## .gitignore
Lists files Git should never track. .env must always be here.
If credentials are accidentally committed, rotate them immediately.
 
## SECRET_KEY
Required by Flask for sessions and flash messages.
Any secret string works in development; use a long random value in prod.
 
## 12-Factor App — Config rule
Store all config (URLs, passwords, keys) in the environment,
never in source code.
 
# From v3
## url_for()          — safe link generation
## Multiple routes    — each @app.route() is a separate handler

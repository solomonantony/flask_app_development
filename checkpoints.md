# Checkpoints — v4
 
1. Visit /config-check. Does it show your DATABASE_URL? Good.
   Now remove that route and commit.
 
2. Delete .env temporarily. What error appears on startup?
   Restore it.
 
3. Run `git status`. Is .env listed? It should NOT be.
   Run `git ls-files`. Is .env in the tracked list?
 
4. What happens if SECRET_KEY is missing and you try to use
   flash messages (coming in v12)?

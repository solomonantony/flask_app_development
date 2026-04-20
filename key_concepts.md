# Key Concepts — v3
 
## url_for('function_name')
Generates the URL for a view function by name.
Use this instead of hard-coding /students so links stay correct
if you ever rename a route.
 
## Multiple routes
Each @app.route() registers a separate URL handler.
The function name becomes the endpoint name used by url_for().
 
## Navigation duplication
Both templates repeat the <nav> block. This will be fixed by
Jinja2 template inheritance (extends/block) in a future refactor.
 
# From v2
## render_template()  — returns an HTML response from a file
## Jinja2 {{ }}       — output expressions in templates

### Flask sample code
For self-reference only ([source - realpython.com](http://realpython.com))

### How to run
- Copy `project/_config.example.py` into `project/_config.py`
- Open `project/_config.py`, replace `<input-your-own-secret!!>` with your own secret
- Run `python db_create.py` to create initial DB (Note: dummy data not working structure is fine)
- Run `python run.py`
- Browse `localhost:5000`

### Flask add-on used
- Flask-WTF
- Flask-SQLAlchemy

### Notes to self
###### Part 2
- DB move from sqlite to `SQLAlchemy` over sqlite, need of `Flask.g` removed as well
- CSRF token `{{ form.csrf_token }}` add for new task form @ `tasks.html`

###### Part 1
- Best practice of `Flask.g` for database within session ([ref](https://stackoverflow.com/questions/15083967/when-should-flask-g-be-used))
- Config with `module`
- `Typed` dynamic route
- `Form` render with `Flask-WTF`
- Use of function `flash` and template `{% for message in get_flashed_messages() %}`
- return (response, status, headers) | best practice: assign status code when build RESTful API
- Use of `session['logged_in'] = True`

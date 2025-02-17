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
- coverage
- nose
- flask-bcrypt

### HTML/CSS Mats
###### Reference
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element
- https://cssvalues.com/

###### Learn
- https://www.codecademy.com/learn/learn-html
- [CSS game](http://flukeout.github.io/)

### Other reference
- [Password storage](https://www.owasp.org/index.php/Secure_Coding_Cheat_Sheet#Password_Storage)

### Notes to self

###### Part 8
- Added RESTful API
- Use of `make_response` to override error code (Can also modify headers if needed)

###### Part 5
- Refactor into `Blueprint`
- Add password hashing
- Add customer error page

###### Part 4
- Added `nose` test and `test coverage`

###### Part 3
- `form.errors` contains errors return from validator
- `def flash_errors` @ `views.py` look really nice but is not used (it also introduce the use of flash()'s category parameter)
- Added `unittest`
- Use of `app.post` @ `test.py` to test route
- the test `test_users_cannot_complete_tasks_that_are_not_created_by_them` is still failing

###### Part 2
- DB move from sqlite to `SQLAlchemy` over sqlite, need of `Flask.g` removed as well
- CSRF token `{{ form.csrf_token }}` add for new task form @ `tasks.html`

###### Part 1
- Best practice of `Flask.g` for database within session ([ref](https://stackoverflow.com/questions/15083967/when-should-flask-g-be-used))
- Config with `module` (Instance folder for secret hanlding - [ref](https://exploreflask.com/en/latest/configuration.html))
- `Typed` dynamic route
- `Form` render with `Flask-WTF`
- Use of function `flash` and template `{% for message in get_flashed_messages() %}`
- return (response, status, headers) | best practice: assign status code when build RESTful API
- Use of `session['logged_in'] = True`

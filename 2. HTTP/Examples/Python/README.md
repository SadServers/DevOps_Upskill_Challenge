# Python Example

Requires Python and the Python `flask` library, install with: `pip install flask`.

To separate Python packages from different projects so they don't conflict with each other, an option is to create a Python virtual environment first: 

```
python -m venv .venv
source .venv/bin/activate
```

(Python packaging is a complex topic and outside the scope of this example)

Now you can `pip install flask` without affecting other Python projects in your computer, or better yet, you can install the exact dependencies provided in this example with: `pip install -r requirements.txt`. The result is the same but it's better to have a manifest with the specific libraries needed and their versions that are known to work with the application.

Run the application with: `python webapp.py`. 
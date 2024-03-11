# Python Syllabus

## Possible materials for the curriculum

Text-only:

* [Official Python Tutorial](https://docs.python.org/3/tutorial/)
* [Pydon'ts](https://mathspp.gumroad.com/l/pydonts)
* [Fluent Python (Second Edition)](https://www.oreilly.com/library/view/fluent-python-2nd/9781492056348/)
* https://realpython.com/learning-paths/writing-pythonic-code/

Video lectures:

* [Some Udemy course](https://www.udemy.com/course/complete-python-bootcamp/)
  (free [via learn.gov.sg](https://learncsc.udemy.com/course/complete-python-bootcamp/))
  (course materials are `ipynb`s: https://github.com/Pierian-Data/Complete-Python-3-Bootcamp)
* [Another Udemy course](https://www.udemy.com/course/master-python-programming-complete-python-bootcamp)
  (free [via learn.gov.sg](https://learncsc.udemy.com/course/master-python-programming-complete-python-bootcamp/))
* [Python for Everyone](https://www.py4e.com)
* [Talks by Raymond Hettinger](https://youtube.com/playlist?list=PLRVdut2KPAguz3xcd22i_o_onnmDKj3MA)

Interactive (write code):

* https://www.learnpython.org
* [Think Python, Third Edition](https://allendowney.github.io/ThinkPython/) (`ipynb`s in colab)

## Syllabus

### Builtins

#### Types

* Numeric (immutable): `bool` (and truthy/falsy values), `int`, `float`, `complex`, `Fraction`, `Decimal`
* Sequences (immutable): `str` (and f-strings), `bytes`, `tuple`, `frozenset`
* Sequences (mutable): `bytearray`, `list`, `set`, generators (e.g. `('abc' * x for x in range(10) if x % 2)`)
* Mappings (mutable): `dict`, `collections.Counter`, `collections.deque`, `collections.defaultdict`
* Singletons (immutable): `None`, `Ellipsis`
* File objects, `BytesIO`, `StringIO`
* Exceptions

#### Operators and operations

* `print`, `pprint.pprint`
* type casting (`int`, `str`/`repr`, `bool`, ...)
* (optional?) bitwise operations
* arithmetic operations
* comparisons (value, identity, membership)
* `min`, `max`, `all`, `any`, `len`, `sum`, `itertools.reduce`
* `map`, `sorted`, `reversed`, `zip`, `range`, `enumerate`
* `functools.partial`
* assignments ~~and the walrus operator~~
    * atomic assignments and swaps (`x, y = y, x`)

#### Modules

* `datetime`, `time`
* `re` (also please go learn regex)
* `enum`, `dataclasses`
* `typing`, `unittest`
* `os`, `pathlib`
* `json`, `base64`, `pickle`, `csv`
* `random`, `secrets`
* `logging`
* `functools`, `itertools`
* (optional?) `threading`, `multiprocessing`
* (optional?) `unittest` (mock and patch), `doctest`
* (optional?) `pdb`

#### Dunder means double-under(score)

* `__name__` (and why/when it equals `"__main__"`)
* `__all__`
* `__file__`
* `__init__` (both the module file and the constructor method)

#### Control flow

Loops:

* `for`-`else`
    * `break`, `continue`
* `while`-`else`
    * `break`, `continue`

Conditionals:

* `if`-`elif`-`else`
    * inline conditionals
* `match`-`case`

Functions and classes:

* functions, generators, and lambdas (`def f(x): ...` or `lambda x: ...`)
    * `return`, `yield`, `x = yield`
    * special arguments: `*args`, `**kwargs`, `*`, `/`
    * argument types
    * decorators (`functools.cache`/`lru_cache`, `functools.wraps`)
    * ~~closures~~
* coroutines (`async def ...`) and `await`
* classes (`class A(list): ...`), class instances (`a = A()`), and methods (`a.sort()`)
    * basic OOP stuff
    * avoid `__call__` unless absolutely necessary

Exception handling and context managers:

* `try`-`except`-`else`-`finally`
    * `raise`
* assertions (`assert maximum >= minimum`)
* `with`
    * `__enter__`, `__exit__`

### Other stuff

* types:
    * type declarations and type checking
    * duck typing and gradual typing
    * (optional?) type definitions (new in Python 3.12: `type Point = tuple[float, float]`)
* modules and imports
* `global`, `nonlocal`, circular imports
* working with containers (and generators):
    * indexing and assignment
    * `del`
    * `iter()`, `next()`
    * packing and unpacking (e.g. splat)
    * comprehensions (for dict, list, and set)
* security
    * `secrets` vs `random`
    * `getpass` vs `input`
    * `hashlib` and `cryptography`
* namespaces and scopes
* paradigms
    * what is OOP and how to do it
    * functional programming and side-effect-free behavior
    * aspect oriented programming
    * `async` and `await`
* (optional?) algorithms and complexity
    * python's builtin sort is much faster than you may expect
    * the `in` operator for substring search is also surprisingly well-optimized

#### Ecosystem

Libraries: `requests` (optionally also `bs4`), `pyyaml`
Libraries (data science): `pandas`, `numpy`/`scipy`, `nltk`, `scikit-learn`, `xgboost`, `shap`
Frameworks: `fastapi` (or `django`/`flask`/`tornado`/`starlette`/...), `pydantic`, `sqlalchemy`, `sqlmodel`
Linting: `flake8`/`ruff` (and go learn about cyclomatic complexity), `mypy`/`pyright`, optionally `yapf`/`black`
Testing: `pytest` (and doctests), `hypothesis`

Tooling:

* pip
* idle
* jupyter
* `twine`/`flit`

#### Code Style

* formatting/whitespace
* naming (`snake_case` for variables, `CamelCase` for classes)
* docstrings and comments
* `import this`
* use comprehensions instead of simple loops
* boolean short-circuiting instead of ternaries
* idioms (e.g., https://en.wikibooks.org/wiki/Python_Programming/Idioms)
    * the EAFP principle
    * note also the string builder idiom
* (optional?) programming patterns (e.g., https://python-patterns.guide)

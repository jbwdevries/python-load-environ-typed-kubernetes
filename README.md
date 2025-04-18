# load-environ-typed-kubernetes

Extends load-environ-typed to get info right from Kubernetes API
## Getting started

```python
from load_environ_typed import load

from dataclasses import dataclass

@dataclass
class MyEnviron:
	db_host: str
	db_port: int

environ = load(MyEnviron)
```

## Contributing

Check out this repo, and then use the following steps to test it:

```sh
python3 -m venv venv
venv/bin/pip install -r requirements-dev.txt
make test
```

## Deploying

First, update pyproject.toml with the new version number, and commit that.

Then:

```sh
rm -f dist/* # Clean old build files
venv/bin/python -m build
venv/bin/python -m twine upload dist/*
```

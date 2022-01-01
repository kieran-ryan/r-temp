init:
	python -m venv venv
	. venv/bin/activate && pip install --requirement requirements-dev.txt
	git submodule update --init --recursive

coverage:
	pytest --cov-report term --cov-report html --cov-report xml --cov=src

publish:
	pip install twine
	python -m build
	python -m twine upload --repository testpypi dist/*
	rm -rf dist pysamplelib.egg-info

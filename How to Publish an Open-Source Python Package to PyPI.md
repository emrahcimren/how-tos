Install twine upload your package to PyPI
```
pip install twine
```

Build your package
```
python setup.py sdist bdist_wheel
```

Check that your package description will render properly on PyPI
```
twine check dist/*
```

Upload to TestPyPI to make sure everything works as expected
- Twine will ask you for your username and password.
```
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

Install your package from test PyPi to see if it is working

```
pip install --index-url https://test.pypi.org/simple/ cimren-wkmeans-geo
```

Upload to PyPI
```
twine upload dist/*
```

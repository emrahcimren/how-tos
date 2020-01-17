1. Install twine upload your package to PyPI
```
pip install twine
```

2. Build your package
```
python setup.py sdist bdist_wheel
```

3. Check that your package description will render properly on PyPI
```
twine check dist/*
```

4. Upload to TestPyPI to make sure everything works as expected
- Twine will ask you for your username and password.
```
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

5. Install your package from test PyPi to see if it is working
```
pip install --index-url https://test.pypi.org/simple/ cimren-wkmeans-geo
```

6. Upload to PyPI
```
twine upload dist/*
```

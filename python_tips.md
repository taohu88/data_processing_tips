# Read whole files
```python
with open('data.txt', 'r') as myfile:
  data = myfile.read()
```
# detect BOM
```python
#!/usr/bin/env python
import chardet # $ pip install chardet

# detect file encoding
with open(filename, 'rb') as file:
    raw = file.read(32) # at most 32 bytes are returned
    encoding = chardet.detect(raw)['encoding']

with open(filename, encoding=encoding) as file:
    text = file.read()
print(text)
```

# pebutcher

pebutcher, Portable Executable reader and alteration module

This project is a fork from the awesome pefile project : https://github.com/erocarrera/pefile

## Features

### Add a new section to the pe file

```
from pebutcher import PE

pe = PE("/tmp/test.exe")
section_data = b"sectionData"
pe.add_section(".sect", 0x60000020, data=section_data)

```
 
### Set section data

```
for pebutcher import PE

pe = PE("/tmp/test.exe")
section_data = b"sectionData"
section = pe.sections[-1]
section.set_data(section_data)

```

### Add a new entries to the import table

```
for pebutcher import PE

pe = PE("/tmp/test.exe")
pe.add_new_imports({"USER32.dll": ["MessageBoxA"]})

```

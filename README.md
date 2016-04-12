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


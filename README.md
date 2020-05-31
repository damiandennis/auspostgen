# Australia Post Barcode Generator

A simple barcode generator currently only supporting x64 linux written for python.

This library makes use of the provided C library provided by Australia Post to generate the barcode value 
and Pillow is used to generate the barcode image. This is quite fast approx 10000 unique barcode images generated in 30 seconds.

### Installation
```bash
python -m pip install auspost
```

### Usage
#### 
```python
from auspost import build_barcode, write_barcode_to_image_file

barcode = build_barcode('11', '59564391')
write_barcode_to_image_file(barcode, './my-barcode37.png')
barcode = build_barcode('59', '59564391', '11ABA 9')
write_barcode_to_image_file(barcode, './my-barcode52.png')
barcode = build_barcode('62', '59564391', '11ABA 911ABA 9')
write_barcode_to_image_file(barcode, './my-barcode67.png')

```


![Barcode37](my-barcode37.png)

![Barcode52](my-barcode52.png)

![Barcode67](my-barcode67.png)
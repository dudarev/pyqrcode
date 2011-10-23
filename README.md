Forked from http://code.google.com/p/pyqrcode/

Usage:

```python
import pyqrcode

qr_image = pyqrcode.MakeQRImage("http://code.google.com/p/pyqrcode/")
qr_image.show()
```

This fork fixes a bug when image size could not be specified in parameters:

```python
qr_code = pyqrcode.MakeQR("test test")
qr_image = qr_code.make_image(block_in_pixels=50, border_in_blocks=0)
qr_image.save("qr.gif", "GIF")
```

To use it with pip include the following line into `requirements.txt`:


```
-e git+git://github.com/dudarev/pyqrcode.git#egg=pyqrcode
```

and then `pip install -E . -r requirements.txt` (if using withing virtualenv, otherwise omit `-E .`).

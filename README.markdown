pyzxing: a qrcode reader  
Author: Andrew Miller <amiller@dappervision.com>  
License: AGPL V3

Wraps the Zebra-Crossing library (zxing/cpp). Works with numpy arrays or PIL Images.

Requirements:  
- numpy  
- PIL (optional)  
- Cython (optional)  

Example 1:

     url = 'http://i.imgur.com/N5ill.jpg'  # Search the web for qrcode photos
     img = Image.open(StringIO.StringIO(urllib2.urlopen(url).read()))
     decoded = pyzxing.decode_image(img)
     print(url, decoded)

Example 2:

     img = Image.open('tests/samples/qr-code.jpg')
     decoded = pyzxing.decode_image(img)
     print(url, decoded)  


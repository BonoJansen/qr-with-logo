**_qr-with-logo_** is a Node package developed to allow for the creation of QR codes with embedded logo images.

##### This is a customized version of qr-with-logo, don't report any error to the real qr-with-logo github or support server. This ripo won't receive support in any way, it will probably not be updated any time soon

## Saving as PNG

```node
const QRLogo = require('qr-with-logo');

const data = JSON.stringify({name: "Zacharie Happel",
              job:  "Student/Intern", 
              grade: "Senior",
              width : 200,
              height : 200
})
 
await QRLogo.generateQRWithLogo(data, "logo.png", {}, "PNG", "qrlogo.png") 

```
## Base64 

```node
const QRLogo = require('qr-with-logo');

const data = JSON.stringify({name: "Zacharie Happel",
              job:  "Student/Intern", 
              grade: "Senior",
              width : 200,
              height : 200
})
 
await QRLogo.generateQRWithLogo(data, "logo.png", {}, "Base64", "qrlogo.png", async function(b64) {
              console.log("Base64: \n" + b64);
}); 

```



## Information 
QRLogo currently only supports saving images as PNG and the exportation of Base64 formatted data. 

 [qrcode](https://www.npmjs.com/package/qrcode) to facilitate the creation of the QR codes, and the [sharp](https://www.npmjs.com/package/sharp) npm package as the means to which images are overlaid. 

qrcode [options](https://www.npmjs.com/package/qrcode#example-1)  may be included when creating the QR code image:

```node
const opts = {
   errorCorrectionLevel:'H',
   rendererOpts: { quality: 0.3 }
}; 

```
## Example Input/Output:
### Logo Image:
![Logo](docs/README-images/logo.png)
### QR Code:
![QR](docs/README-images/qrlogo.png) 

## License
[MIT](https://choosealicense.com/licenses/mit/)
# USB Token drivers

Packages for support of some USB Token on (X|L)Ubuntu 20.04 / 22.04 LTS

## USB Tokens supported

- GD StarSign Crypto
- Aladdin eToken PRO USB 72k

## After Install

There are the follows libraries to add on your browser:

- GD StarSign Crypto (`/usr/lib/libaetpkss.so`)
- Aladdin eToken PRO USB 72k (`/usr/lib/libeTPkcs11.so`)

Close firefox and Google Chrome then run:

```bash
modutil -dbdir sql:.pki/nssdb/ -add "usbToken" -libfile /lib/of/your/usb/token.so
```

Check if was installed:

```bash
modutil -dbdir sql:.pki/nssdb/ -list
```

For Firefox you need add manually.
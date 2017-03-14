# apns-pusher

> apns-pusher use to test apns push service. you can use it to push some simple message to apns.

## Prepare

Before use this tool you must prepare like follow:

##### 1. Install python on your pc (Most computers have their own)，type follow command to check.

```
python --version
```

##### 2. Install apns module, you can use easy_install or pip to install it 

```
easy_install apns

or 

pi install apns
```

##### 3. export cert.p12 and key.p12. Go to 'Keychain Access' and export like follow(Must on Mac OS):

```
For Develop

├── Apple Development IOS Push Services: com.apple.test     - right click to export cert.p12
│   └── xxxx                                                - right click to export key.p12

For Release(Apple Store)

├── Apple Push Services: com.apple.test                     - right click to export cert.p12
│   └── xxxx                                                - right click to export key.p12

```

##### 4. use `pem-generator` to generate cert.pem and key.pem

```
chmod +x pem-generator 
./pem-generator cert.p12 key.p12
```
PS: Will generate cert.pem and key.pem in current directory.

## Usage 

For Develop

```
chmod +x apns-develop-pusher
./apns-develop-pusher 9e31c2f3c5d9b21a006996f1ae772b205d0c1115671e5b64f7a779ff1e0b1 hello
```

For Release(Apple Store)

```
chmod +x apns-release-pusher
./apns-release-pusher 9e31c2f3c5d9b21a006996f1ae772b205d0c1115671e5b64f7a779ff1e0b1 hello
```

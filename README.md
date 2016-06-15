# docket

A certificate generation tool written in Go (Golang).

[![](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat-square)](https://godoc.org/github.com/abcum/docket) [![](https://goreportcard.com/badge/github.com/abcum/docket?style=flat-square)](https://goreportcard.com/report/github.com/abcum/docket) [![](https://img.shields.io/badge/license-Apache_License_2.0-blue.svg?style=flat-square)](https://github.com/abcum/docket) 

#### Features

- Simple cli interface
- Defaults are optimised for security
- Create CAs for distributed services
- Create client authentication certificates
- Create cluster authentication certificates
- Create rsa encryption private + public key pairs
- Can be used to create self-signed development certificates
- Secure distributed services using dns names or ip addresses
- Makes use of golang crypto packages internally to create certificates 

#### Installation

```
go get github.com/abcum/docket
```

#### Example usage

```
docket ca --out-crt ca.crt --out-key ca.key
```

```
docket client --ca-crt ca.crt --ca-key ca.key --out-crt client.crt --out-key client.key
```

```
docket server --ca-crt ca.crt --ca-key ca.key --out-crt server.crt --out-key server.key example.com
```

```
docket server --ca-crt ca.crt --ca-key ca.key --out-crt server.crt --out-key server.key 10.0.1.1 10.0.1.2 10.0.1.3
```
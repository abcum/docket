# docket

A certificate generation tool written in Go (Golang).

[![](https://img.shields.io/badge/status-v1-ff00bb.svg?style=flat-square)](https://github.com/abcum/docket) [![](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat-square)](https://godoc.org/github.com/abcum/docket) [![](https://goreportcard.com/badge/github.com/abcum/docket?style=flat-square)](https://goreportcard.com/report/github.com/abcum/docket) [![](https://img.shields.io/badge/license-Apache_License_2.0-00bfff.svg?style=flat-square)](https://github.com/abcum/docket) 

#### Features

- Simple cli interface
- Defaults are optimised for security
- Create CAs for distributed services
- Create client authentication certificates
- Create server authentication certificates
- Create cluster authentication certificates
- Create rsa encryption private + public key pairs
- Can be used to create self-signed development certificates
- Secure distributed services using dns names or ip addresses
- Makes use of golang crypto packages internally to create certificates 

#### Installation

```bash
go get github.com/abcum/docket
```

#### Example usage

```bash
docket ca --out-org Abcum --out-crt ca.crt --out-key ca.key
```

```bash
docket client --ca-crt ca.crt --ca-key ca.key --out-org Abcum --out-crt client.crt --out-key client.key
```

```bash
docket server --ca-crt ca.crt --ca-key ca.key --out-org Abcum --out-crt server.crt --out-key server.key example.com
```

```bash
docket server --ca-crt ca.crt --ca-key ca.key --out-org Abcum --out-crt server.crt --out-key server.key 10.0.1.1 10.0.1.2 10.0.1.3
```

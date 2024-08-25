# Unifi Access API Protobuf Definitions

**Version:** V2.2.10

**Documentation:** https://core-config-gfoz.uid.alpha.ui.com/configs/unifi-access/api_reference.pdf

## Overview

This repository provides protobuf definitions for the Ubiquiti Access API, allowing developers to generate client libraries, validate messages, and define services for integration with Ubiquiti Access systems. These definitions are intended for use in creating message and service definitions, and are not tied to any specific server implementation.

## Disclaimer

This is unofficial API documentation for the Ubiquiti Access API. It is provided as-is without any guarantees of accuracy or completeness. Use at your own risk.

## API Documentation

[View API Documentation](https://htmlpreview.github.io/?https://github.com/luis-godinez/Unifi-Access-API/blob/main/docs/index.html)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/luis-godinez/Unifi-Access-API.git
cd unifi-access-api
```

### 2. Install Dependencies

`npm install`

### 3. Generate Code

Javascript `npm run generate:js`

Typescript: `npm run generate:ts`

### 4. Use in your project

Javascript(commonJS):  
`const { Visitor } = require('../path/to/generated/dist/visitor_pb.js');`

Javascript(ES6):  
`import { Visitor } from '../path/to/generated/dist/visitor_pb.js';`

Typescript:  
`import { Visitor } from '../path/to/generated/dist/visitor_pb';`

## Contribution:

If you'd like to contribute to this project due to any API changes or issues, please ensure to:
* update the README documentation w/ latest API version
* re-generate the API documentation

### Generate documentation from proto definition

```
go install github.com/pseudomuto/protoc-gen-doc/cmd/protoc-gen-doc@latest
protoc --doc_out=./docs --doc_opt=html,index.html proto/*.proto
```

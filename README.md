<!--
Copyright 2018 Adobe. All rights reserved.
This file is licensed to you under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License. You may obtain a copy
of the License at http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under
the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR REPRESENTATIONS
OF ANY KIND, either express or implied. See the License for the specific language
governing permissions and limitations under the License.
-->

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/@adobe/aio-cli-plugin-jwt-auth.svg)](https://npmjs.org/package/@adobe/aio-cli-plugin-jwt-auth)
[![Downloads/week](https://img.shields.io/npm/dw/@adobe/aio-cli-plugin-jwt-auth.svg)](https://npmjs.org/package/@adobe/aio-cli-plugin-jwt-auth)
[![Build Status](https://travis-ci.org/adobe/aio-cli-plugin-jwt-auth.svg?branch=master)](https://travis-ci.org/adobe/aio-cli-plugin-jwt-auth) 
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Greenkeeper badge](https://badges.greenkeeper.io/adobe/aio-cli-plugin-jwt-auth.svg)](https://greenkeeper.io/)
[![Codecov Coverage](https://img.shields.io/codecov/c/github/adobe/aio-cli-plugin-jwt-auth/master.svg?style=flat-square)](https://codecov.io/gh/adobe/aio-cli-plugin-jwt-auth/)

aio-cli-plugin-jwt-auth
=======================

JWT Auth Plugin for the Adobe I/O CLI

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @adobe/aio-cli-plugin-jwt-auth
$ ./bin/run COMMAND
running command...
$ ./bin/run (-v|--version|version)
@adobe/aio-cli-plugin-jwt-auth/1.0.9 darwin-x64 node-v8.11.2
$ ./bin/run --help [COMMAND]
USAGE
  $ ./bin/run COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`./bin/run jwt-auth:access-token`](#bin-run-jwt-authaccess-token)

## `./bin/run jwt-auth:access-token`

get the access token for the Adobe I/O Console

```
USAGE
  $ ./bin/run jwt-auth:access-token

OPTIONS
  -p, --passphrase=passphrase  the passphrase for the private-key

DESCRIPTION
  You must have a 'jwt-auth' key in your config, that has all your config data in .json format:
       aio config:set jwt-auth path/to/your/config.json --file --mime-type=application/json

EXAMPLE

  jwt_auth:
  {
     "client_id": "...",
     "client_secret": "...",
     "token_exchange_url": "...",
     "jwt_payload": {
       "iss": "...",
       "sub": "...",
       "...": true,
       "aud": "..."
     },
     "jwt_private_key": [
       "-----BEGIN RSA PRIVATE KEY-----",
       "...",
       "...",
       "...==",
       "-----END RSA PRIVATE KEY-----"
     ],
     "console_get_orgs_url":"...",
     "console_get_namespaces_url":"..."
  }
```

_See code: [src/commands/jwt-auth/access-token.js](https://github.com/adobe/aio-cli-plugin-jwt-auth/blob/v1.0.9/src/commands/jwt-auth/access-token.js)_
<!-- commandsstop -->

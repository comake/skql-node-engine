[![npm version](https://badge.fury.io/js/@comake%2Fskql-node-engine.svg)](https://badge.fury.io/js/@comake%2Fskql-node-engine) [![License](https://img.shields.io/badge/License-BSD_4--Clause-blue.svg)](https://spdx.org/licenses/BSD-4-Clause.html)

# SKQL Node Engine

This is a Node.js implementation of a Standard Knowledge Query Language Engine for [Standard Knowledge Language (SKL)](https://www.comake.io/skl). It is written in Typescript and follows the [SKL Engine specification](https://docs.standardknowledge.com/get-started/engine).

## How to use SKQL Node Engine

#### Requirements
- Node.js
- Java VM

#### 1. Install via npm or yarn:

```shell
npm install @comake/skql-node-engine
yarn add @comake/skql-node-engine
```

#### 2. Define Schemas

We will be posting more documentation on schemas soon. For now, you can view examples of schemas in use in the [examples folder of skql-node-engine](https://github.com/comake/skql-node-engine/tree/main/examples).

 The [folder-structure-sync](https://github.com/comake/skql-node-engine/tree/main/examples/folder-structure-sync) example is a node.js module that can recursively loop through the folder structure of any Integration that works with the `getFilesInFolder` Verb.

#### 3. Write code

Once you have schemas defined for your domain, all you have to do is write code using the Verbs and Nouns in your schema to build your application logic.


## How to contribute

#### Requirements
- Node.js
- Java VM
- Jar of the RMLMapper, which you can download (see step 2).

#### 1. Clone the repo

To clone the repo, execute the following commands in your terminal:
```shell
git clone https://github.com/comake/skql-node-engine.git
cd skql-node-engine
npm ci
```

#### 2. Download RMLMapper

Download the latest release of the RMLMapper jar from its [releases page](https://github.com/RMLio/rmlmapper-java/releases/). Put the jar file in a folder called `lib` at the top level of your local clone of this repo. Change this line in [src/Mapper.ts](https://github.com/comake/skql-node-engine/blob/main/src/Mapper.ts) to use the correct filename for the release you're using:
```
const rmlmapperPath = path.join(__dirname, '/../lib/rmlmapper-6.0.0-r363-all.jar');
```

# License & Copyright

SKQL Javascript Engine is available under the BSD 4 license. See the [LICENSE](LICENSE) file for more info.

Copyright (c) 2022, Comake, Inc.

# TODO

- [ ] add husky
- [ ] unhardcode rml path
- [ ] add README to example
- [ ] add CONTRIBUTING.md, CODE_OF_CONDUCT.md, etc
- [ ] add skds schema source

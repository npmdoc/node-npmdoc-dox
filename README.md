# api documentation for  [dox (v0.9.0)](https://github.com/tj/dox)  [![npm package](https://img.shields.io/npm/v/npmdoc-dox.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dox) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dox.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dox)
#### Markdown / JSdoc documentation generator

[![NPM](https://nodei.co/npm/dox.png?downloads=true)](https://www.npmjs.com/package/dox)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dox/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-dox_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dox/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dox/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dox/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk",
        "email": "tj@vision-media.ca"
    },
    "bin": {
        "dox": "./bin/dox"
    },
    "bugs": {
        "url": "https://github.com/visionmedia/dox/issues"
    },
    "contributors": [
        {
            "name": "Jarvis Badgley",
            "email": "chiper@chipersoft.com"
        },
        {
            "name": "Arseny Zarechnev",
            "email": "me@evindor.com"
        },
        {
            "name": "Thomas Parisot",
            "email": "hi@oncletom.io"
        },
        {
            "name": "Stephen Mathieson",
            "email": "me@stephenmathieson.com"
        },
        {
            "name": "Vladimir Tsvang",
            "email": "vtsvang@gmail.com"
        },
        {
            "name": "Nathan Rajlich",
            "email": "nathan@tootallnate.net"
        },
        {
            "name": "Gion Kunz",
            "email": "gion.kunz@gmail.com"
        },
        {
            "name": "ForbesLindesay"
        }
    ],
    "dependencies": {
        "commander": "~2.9.0",
        "jsdoctypeparser": "^1.2.0",
        "markdown-it": "~7.0.0"
    },
    "description": "Markdown / JSdoc documentation generator",
    "devDependencies": {
        "mocha": "~3.0.2",
        "should": "~11.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "be97b085cb9f4a0b7e80835d547e77b8687d0a0c",
        "tarball": "https://registry.npmjs.org/dox/-/dox-0.9.0.tgz"
    },
    "gitHead": "31c161d2ff98f55c56f911fcf6b6211dfb2e0965",
    "homepage": "https://github.com/tj/dox",
    "keywords": [
        "documentation",
        "docs",
        "markdown",
        "jsdoc"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "evindor",
            "email": "me@evindor.com"
        },
        {
            "name": "chipersoft",
            "email": "chiper@chipersoft.com"
        }
    ],
    "name": "dox",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/visionmedia/dox.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "0.9.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module dox](#apidoc.module.dox)
1.  [function <span class="apidocSignatureSpan">dox.</span>api (comments)](#apidoc.element.dox.api)
1.  [function <span class="apidocSignatureSpan">dox.</span>extractTagParts (str)](#apidoc.element.dox.extractTagParts)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseCodeContext (str, parentContext)](#apidoc.element.dox.parseCodeContext)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseComment (str, options)](#apidoc.element.dox.parseComment)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseComments (js, options)](#apidoc.element.dox.parseComments)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseParamOptional (tag)](#apidoc.element.dox.parseParamOptional)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseTag (str)](#apidoc.element.dox.parseTag)
1.  [function <span class="apidocSignatureSpan">dox.</span>parseTagTypes (str, tag)](#apidoc.element.dox.parseTagTypes)
1.  [function <span class="apidocSignatureSpan">dox.</span>trimIndentation (str)](#apidoc.element.dox.trimIndentation)
1.  object <span class="apidocSignatureSpan">dox.</span>contextPatternMatchers
1.  object <span class="apidocSignatureSpan">dox.</span>utils

#### [module dox.contextPatternMatchers](#apidoc.module.dox.contextPatternMatchers)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>0 (str)](#apidoc.element.dox.contextPatternMatchers.0)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>1 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.1)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>10 (str)](#apidoc.element.dox.contextPatternMatchers.10)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>11 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.11)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>12 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.12)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>13 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.13)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>14 (str)](#apidoc.element.dox.contextPatternMatchers.14)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>15 (str)](#apidoc.element.dox.contextPatternMatchers.15)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>16 (str)](#apidoc.element.dox.contextPatternMatchers.16)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>2 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.2)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>3 (str)](#apidoc.element.dox.contextPatternMatchers.3)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>4 (str)](#apidoc.element.dox.contextPatternMatchers.4)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>5 (str)](#apidoc.element.dox.contextPatternMatchers.5)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>6 (str)](#apidoc.element.dox.contextPatternMatchers.6)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>7 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.7)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>8 (str)](#apidoc.element.dox.contextPatternMatchers.8)
1.  [function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>9 (str)](#apidoc.element.dox.contextPatternMatchers.9)

#### [module dox.utils](#apidoc.module.dox.utils)
1.  [function <span class="apidocSignatureSpan">dox.utils.</span>escape (html)](#apidoc.element.dox.utils.escape)



# <a name="apidoc.module.dox"></a>[module dox](#apidoc.module.dox)

#### <a name="apidoc.element.dox.api"></a>[function <span class="apidocSignatureSpan">dox.</span>api (comments)](#apidoc.element.dox.api)
- description and source-code
```javascript
api = function (comments){
  var buf = [];

  comments.forEach(function(comment){
    if (comment.isPrivate) return;
    if (comment.ignore) return;
    var ctx = comment.ctx;
    var desc = comment.description;
    if (!ctx) return;
    if (~desc.full.indexOf('Module dependencies')) return;
    if (!ctx.string.indexOf('module.exports')) return;
    buf.push('### ' + context(comment));
    buf.push('');
    buf.push(desc.full.trim().replace(/^/gm, '  '));
    buf.push('');
  });

  buf = buf
    .join('\n')
    .replace(/^ *#/gm, '')

  var code = buf.match(/^( {4}[^\n]+\n*)+/gm) || [];

  code.forEach(function(block){
    var code = block.replace(/^ {4}/gm, '');
    buf = buf.replace(block, ''''js\n' + code.trimRight() + '\n'''\n\n');
  });

  return toc(buf) + '\n\n' + buf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.extractTagParts"></a>[function <span class="apidocSignatureSpan">dox.</span>extractTagParts (str)](#apidoc.element.dox.extractTagParts)
- description and source-code
```javascript
extractTagParts = function (str) {
  var level = 0,
    extract = '',
    split = [];

  str.split('').forEach(function(c) {
    if(c.match(/\s/) && level === 0) {
      split.push(extract);
      extract = '';
    } else {
      if(c === '{') {
        level++;
      } else if (c === '}') {
        level--;
      }

      extract += c;
    }
  });

  split.push(extract);
  return split.filter(function(str) {
    return str.length > 0;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.parseCodeContext"></a>[function <span class="apidocSignatureSpan">dox.</span>parseCodeContext (str, parentContext)](#apidoc.element.dox.parseCodeContext)
- description and source-code
```javascript
parseCodeContext = function (str, parentContext) {
  parentContext = parentContext || {};

  var ctx;

  // loop through all context matchers, returning the first successful match
  return exports.contextPatternMatchers.some(function (matcher) {
    return ctx = matcher(str, parentContext);
  }) && ctx;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.parseComment"></a>[function <span class="apidocSignatureSpan">dox.</span>parseComment (str, options)](#apidoc.element.dox.parseComment)
- description and source-code
```javascript
parseComment = function (str, options) {
  str = str.trim();
  options = options || {};

  var comment = { tags: [] }
    , raw = options.raw
    , description = {}
    , tags = str.split(/\n\s*@/);

  // A comment has no description
  if (tags[0].charAt(0) === '@') {
    tags.unshift('');
  }

  // parse comment body
  description.full = tags[0];
  description.summary = description.full.split('\n\n')[0];
  description.body = description.full.split('\n\n').slice(1).join('\n\n');
  comment.description = description;

  // parse tags
  if (tags.length) {
    comment.tags = tags.slice(1).map(exports.parseTag);
    comment.isPrivate = comment.tags.some(function(tag){
      return 'private' == tag.visibility;
    });
    comment.isConstructor = comment.tags.some(function(tag){
      return 'constructor' == tag.type || 'augments' == tag.type;
    });
    comment.isClass = comment.tags.some(function(tag){
      return 'class' == tag.type;
    });
    comment.isEvent = comment.tags.some(function(tag){
      return 'event' == tag.type;
    });

    if (!description.full || !description.full.trim()) {
      comment.tags.some(function(tag){
        if ('description' == tag.type) {
          description.full = tag.full;
          description.summary = tag.summary;
          description.body = tag.body;
          return true;
        }
      });
    }
  }

  // markdown
  if (!raw) {
    description.full = markdown.render(description.full).trim();
    description.summary = markdown.render(description.summary).trim();
    description.body = markdown.render(description.body).trim();
    comment.tags.forEach(function (tag) {
      if (tag.description) tag.description = markdown.render(tag.description).trim();
      else tag.html = markdown.render(tag.string).trim();
    });
  }

  return comment;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.parseComments"></a>[function <span class="apidocSignatureSpan">dox.</span>parseComments (js, options)](#apidoc.element.dox.parseComments)
- description and source-code
```javascript
parseComments = function (js, options){
  options = options || {};
  js = js.replace(/\r\n/gm, '\n');

  var comments = []
    , skipSingleStar = options.skipSingleStar
    , comment
    , buf = ''
    , ignore
    , withinMultiline = false
    , withinSingle = false
    , withinString = false
    , code
    , linterPrefixes = options.skipPrefixes || ['jslint', 'jshint', 'eshint']
    , skipPattern = new RegExp('^' + (options.raw ? '' : '<p>') + '('+ linterPrefixes.join('|') + ')')
    , lineNum = 1
    , lineNumStarting = 1
    , parentContext
    , withinEscapeChar
    , currentStringQuoteChar;


  for (var i = 0, len = js.length; i < len; ++i) {
    withinEscapeChar = withinString && !withinEscapeChar && js[i - 1] == '\\';

    // start comment
    if (!withinMultiline && !withinSingle && !withinString &&
        '/' == js[i] && '*' == js[i+1] && (!skipSingleStar || js[i+2] == '*')) {
      lineNumStarting = lineNum;
      // code following the last comment
      if (buf.trim().length) {
        comment = comments[comments.length - 1];
        if(comment) {
          // Adjust codeStart for any vertical space between comment and code
          comment.codeStart += buf.match(/^(\s*)/)[0].split('\n').length - 1;
          comment.code = code = exports.trimIndentation(buf).trim();
          comment.ctx = exports.parseCodeContext(code, parentContext);

          if (comment.isConstructor && comment.ctx){
              comment.ctx.type = "constructor";
          }

          // starting a new namespace
          if (comment.ctx && (comment.ctx.type === 'prototype' || comment.ctx.type === 'class')){
            parentContext = comment.ctx;
          }
          // reasons to clear the namespace
          // new property/method in a different constructor
          else if (!parentContext || !comment.ctx || !comment.ctx.constructor || !parentContext.constructor || parentContext.constructor
 !== comment.ctx.constructor){
            parentContext = null;
          }
        }
        buf = '';
      }
      i += 2;
      withinMultiline = true;
      ignore = '!' == js[i];

      // if the current character isn't whitespace and isn't an ignored comment,
      // back up one character so we don't clip the contents
      if (' ' !== js[i] && '\n' !== js[i] && '\t' !== js[i] && '!' !== js[i]) i--;

    // end comment
    } else if (withinMultiline && !withinSingle && '*' == js[i] && '/' == js[i+1]) {
      i += 2;
      buf = buf.replace(/^[ \t]*\* ?/gm, '');
      comment = exports.parseComment(buf, options);
      comment.ignore = ignore;
      comment.line = lineNumStarting;
      comment.codeStart = lineNum + 1;
      if (!comment.description.full.match(skipPattern)) {
        comments.push(comment);
      }
      withinMultiline = ignore = false;
      buf = '';
    } else if (!withinSingle && !withinMultiline && !withinString && '/' == js[i] && '/' == js[i+1]) {
      withinSingle = true;
      buf += js[i];
    } else if (withinSingle && !withinMultiline && '\n' == js[i]) {
      withinSingle = false;
      buf += js[i];
    } else if (!withinSingle && !withinMultiline && !withinEscapeChar && ('\'' == js[i] || '"' == js[i] || ''' == js[i])) {
      if(withinString) {
        if(js[i] == currentStringQuoteChar) {
          withinString = false;
        }
      } else {
        withinString = true;
        currentStringQuoteChar = js[i];
      }

      buf += js[i];
    } else {
      buf += js[i];
    }

    if('\n' == js[i]) {
      lineNum++;
    }

  }

  if (comments.length === 0) {
    comments.push({
      tags: [],
      description: {full: '', summary: '', body: ''},
      isPrivate: false,
      isConstructor: false,
      line: lineNumStarting
    });
  }

  // trailing code
  if (buf.trim().length) {
    comment = comments[comments.length - 1];
    // Adjust codeStart for any vertical space between comment and code
    comment.codeStart += buf.match(/^(\s*)/)[0].split('\n').length - 1;
    comment.code = code = exports.trimIndentation(buf).trim();
    comment.ctx = exports.parseCodeContext(code, parentContext);
  }

  return com ...
```
- example usage
```shell
...
### Programmatic Usage

''' javascript

var dox = require('dox'),
    code = "...";

var obj = dox.parseComments(code);

// [{ tags:[ ... ], description, ... }, { ... }, ...]

'''

## Properties
...
```

#### <a name="apidoc.element.dox.parseParamOptional"></a>[function <span class="apidocSignatureSpan">dox.</span>parseParamOptional (tag)](#apidoc.element.dox.parseParamOptional)
- description and source-code
```javascript
parseParamOptional = function (tag) {
  var lastTypeChar = tag.types.slice(-1)[0].slice(-1);
  return tag.name.slice(0,1) === '[' || lastTypeChar === '=' || lastTypeChar === '?';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.parseTag"></a>[function <span class="apidocSignatureSpan">dox.</span>parseTag (str)](#apidoc.element.dox.parseTag)
- description and source-code
```javascript
parseTag = function (str) {
  var tag = {}
    , lines = str.split('\n')
    , parts = exports.extractTagParts(lines[0])
    , type = tag.type = parts.shift().replace('@', '')
    , matchType = new RegExp('^@?' + type + ' *')
    , matchTypeStr = /^\{.+\}$/;

  tag.string = str.replace(matchType, '');

  if (lines.length > 1) {
    parts.push(lines.slice(1).join('\n'));
  }

  switch (type) {
    case 'property':
    case 'template':
    case 'param':
      var typeString = matchTypeStr.test(parts[0]) ? parts.shift() : "";
      tag.name = parts.shift() || '';
      tag.description = parts.join(' ');
      exports.parseTagTypes(typeString, tag);
      break;
    case 'define':
    case 'return':
    case 'returns':
      var typeString = matchTypeStr.test(parts[0]) ? parts.shift() : "";
      exports.parseTagTypes(typeString, tag);
      tag.description = parts.join(' ');
      break;
    case 'see':
      if (~str.indexOf('http')) {
        tag.title = parts.length > 1
          ? parts.shift()
          : '';
        tag.url = parts.join(' ');
      } else {
        tag.local = parts.join(' ');
      }
      break;
    case 'api':
      tag.visibility = parts.shift();
      break;
    case 'public':
    case 'private':
    case 'protected':
      tag.visibility = type;
      break;
    case 'enum':
    case 'typedef':
    case 'type':
      exports.parseTagTypes(parts.shift(), tag);
      break;
    case 'lends':
    case 'memberOf':
      tag.parent = parts.shift();
      break;
    case 'extends':
    case 'implements':
    case 'augments':
      tag.otherClass = parts.shift();
      break;
    case 'borrows':
      tag.otherMemberName = parts.join(' ').split(' as ')[0];
      tag.thisMemberName = parts.join(' ').split(' as ')[1];
      break;
    case 'throws':
      var typeString = matchTypeStr.test(parts[0]) ? parts.shift() : "";
      tag.types = exports.parseTagTypes(typeString);
      tag.description = parts.join(' ');
      break;
    case 'description':
      tag.full = parts.join(' ').trim();
      tag.summary = tag.full.split('\n\n')[0];
      tag.body = tag.full.split('\n\n').slice(1).join('\n\n');
      break;
    default:
      tag.string = parts.join(' ').replace(/\s+$/, '');
      break;
  }

  return tag;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.parseTagTypes"></a>[function <span class="apidocSignatureSpan">dox.</span>parseTagTypes (str, tag)](#apidoc.element.dox.parseTagTypes)
- description and source-code
```javascript
parseTagTypes = function (str, tag) {
  if (!str) {
    if(tag) {
      tag.types = [];
      tag.typesDescription = "";
      tag.optional = tag.nullable = tag.nonNullable = tag.variable = false;
    }
    return [];
  }
  var Parser = require('jsdoctypeparser').Parser;
  var Builder = require('jsdoctypeparser').Builder;
  var result = new Parser().parse(str.substr(1, str.length - 2));

  var types = (function transform(type) {
    if(type instanceof Builder.TypeUnion) {
      return type.types.map(transform);
    } else if(type instanceof Builder.TypeName) {
      return type.name;
    } else if(type instanceof Builder.RecordType) {
      return type.entries.reduce(function(obj, entry) {
        obj[entry.name] = transform(entry.typeUnion);
        return obj;
      }, {});
    } else {
      return type.toString();
    }
  }(result));

  if(tag) {
    tag.types = types;
    tag.typesDescription = result.toHtml();
    tag.optional = (tag.name && tag.name.slice(0,1) === '[') || result.optional;
    tag.nullable = result.nullable;
    tag.nonNullable = result.nonNullable;
    tag.variable = result.variable;
  }

  return types;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.trimIndentation"></a>[function <span class="apidocSignatureSpan">dox.</span>trimIndentation (str)](#apidoc.element.dox.trimIndentation)
- description and source-code
```javascript
trimIndentation = function (str) {
  // Find indentation from first line of code.
  var indent = str.match(/(?:^|\n)([ \t]*)[^\s]/);
  if (indent) {
    // Replace indentation on all lines.
    str = str.replace(new RegExp('(^|\n)' + indent[1], 'g'), '$1');
  }
  return str;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dox.contextPatternMatchers"></a>[module dox.contextPatternMatchers](#apidoc.module.dox.contextPatternMatchers)

#### <a name="apidoc.element.dox.contextPatternMatchers.0"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>0 (str)](#apidoc.element.dox.contextPatternMatchers.0)
- description and source-code
```javascript
0 = function (str) {
  // class, possibly exported by name or as a default
  if (/^\s*(export(\s+default)?\s+)?class\s+([\w$]+)(\s+extends\s+([\w$.]+(?:\(.*\))?))?\s*{/.exec(str)) {
    return {
        type: 'class'
      , constructor: RegExp.$3
      , cons: RegExp.$3
      , name: RegExp.$3
      , extends: RegExp.$5
      , string: 'new ' + RegExp.$3 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.1"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>1 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.1)
- description and source-code
```javascript
1 = function (str, parentContext) {
  // class constructor
  if (/^\s*constructor\s*\(/.exec(str)) {
    return {
      type: 'constructor'
      , constructor: parentContext.name
      , cons: parentContext.name
      , name: 'constructor'
      , string: (parentContext && parentContext.name && parentContext.name + '.prototype.' || '') + 'constructor()'
    };
  // class method
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.10"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>10 (str)](#apidoc.element.dox.contextPatternMatchers.10)
- description and source-code
```javascript
10 = function (str) {
  // inline prototype
  if (/^\s*([\w$.]+)\s*\.\s*prototype\s*=\s*{/.exec(str)) {
    return {
      type: 'prototype'
      , constructor: RegExp.$1
      , cons: RegExp.$1
      , name: RegExp.$1
      , string: RegExp.$1 + '.prototype'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.11"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>11 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.11)
- description and source-code
```javascript
11 = function (str, parentContext) {
  // inline method
  if (/^\s*([\w$.]+)\s*:\s*function/.exec(str)) {
    return {
      type: 'method'
      , constructor: parentContext.name
      , cons: parentContext.name
      , name: RegExp.$1
      , string: (parentContext && parentContext.name && parentContext.name + '.prototype.' || '') + RegExp.$1 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.12"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>12 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.12)
- description and source-code
```javascript
12 = function (str, parentContext) {
  // inline property
  if (/^\s*([\w$.]+)\s*:\s*([^\n;]+)/.exec(str)) {
    return {
      type: 'property'
      , constructor: parentContext.name
      , cons: parentContext.name
      , name: RegExp.$1
      , value: RegExp.$2.trim()
      , string: (parentContext && parentContext.name && parentContext.name + '.' || '') + RegExp.$1
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.13"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>13 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.13)
- description and source-code
```javascript
13 = function (str, parentContext) {
  // inline getter/setter
  if (/^\s*(get|set)\s*([\w$.]+)\s*\(/.exec(str)) {
    return {
      type: 'property'
      , constructor: parentContext.name
      , cons: parentContext.name
      , name: RegExp.$2
      , string: (parentContext && parentContext.name && parentContext.name + '.prototype.' || '') + RegExp.$2
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.14"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>14 (str)](#apidoc.element.dox.contextPatternMatchers.14)
- description and source-code
```javascript
14 = function (str) {
  // method
  if (/^\s*([\w$.]+)\s*\.\s*([\w$]+)\s*=\s*function/.exec(str)) {
    return {
        type: 'method'
      , receiver: RegExp.$1
      , name: RegExp.$2
      , string: RegExp.$1 + '.' + RegExp.$2 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.15"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>15 (str)](#apidoc.element.dox.contextPatternMatchers.15)
- description and source-code
```javascript
15 = function (str) {
  // property
  if (/^\s*([\w$.]+)\s*\.\s*([\w$]+)\s*=\s*([^\n;]+)/.exec(str)) {
    return {
        type: 'property'
      , receiver: RegExp.$1
      , name: RegExp.$2
      , value: RegExp.$3.trim()
      , string: RegExp.$1 + '.' + RegExp.$2
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.16"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>16 (str)](#apidoc.element.dox.contextPatternMatchers.16)
- description and source-code
```javascript
16 = function (str) {
  // declaration
  if (/^\s*(?:const|let|var)\s+([\w$]+)\s*=\s*([^\n;]+)/.exec(str)) {
    return {
        type: 'declaration'
      , name: RegExp.$1
      , value: RegExp.$2.trim()
      , string: RegExp.$1
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.2"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>2 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.2)
- description and source-code
```javascript
2 = function (str, parentContext) {
  if (/^\s*(static)?\s*(\*)?\s*([\w$]+|\[.*\])\s*\(/.exec(str)) {
    return {
      type: 'method'
      , constructor: parentContext.name
      , cons: parentContext.name
      , name: RegExp.$2 + RegExp.$3
      , string: (parentContext && parentContext.name && parentContext.name + (RegExp.$1 ? '.' : '.prototype.') || '') + RegExp.$
2 + RegExp.$3 + '()'
    };
  // named function statement, possibly exported by name or as a default
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.3"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>3 (str)](#apidoc.element.dox.contextPatternMatchers.3)
- description and source-code
```javascript
3 = function (str) {
  if (/^\s*(export(\s+default)?\s+)?function\s+([\w$]+)\s*\(/.exec(str)) {
    return {
        type: 'function'
      , name: RegExp.$3
      , string: RegExp.$3 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.4"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>4 (str)](#apidoc.element.dox.contextPatternMatchers.4)
- description and source-code
```javascript
4 = function (str) {
  // anonymous function expression exported as a default
  if (/^\s*export\s+default\s+function\s*\(/.exec(str)) {
    return {
        type: 'function'
      , name: RegExp.$1 // undefined
      , string: RegExp.$1 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.5"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>5 (str)](#apidoc.element.dox.contextPatternMatchers.5)
- description and source-code
```javascript
5 = function (str) {
  // function expression
  if (/^return\s+function(?:\s+([\w$]+))?\s*\(/.exec(str)) {
    return {
        type: 'function'
      , name: RegExp.$1
      , string: RegExp.$1 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.6"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>6 (str)](#apidoc.element.dox.contextPatternMatchers.6)
- description and source-code
```javascript
6 = function (str) {
  // function expression
  if (/^\s*(?:const|let|var)\s+([\w$]+)\s*=\s*function/.exec(str)) {
    return {
        type: 'function'
      , name: RegExp.$1
      , string: RegExp.$1 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.7"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>7 (str, parentContext)](#apidoc.element.dox.contextPatternMatchers.7)
- description and source-code
```javascript
7 = function (str, parentContext) {
  // prototype method
  if (/^\s*([\w$.]+)\s*\.\s*prototype\s*\.\s*([\w$]+)\s*=\s*function/.exec(str)) {
    return {
        type: 'method'
      , constructor: RegExp.$1
      , cons: RegExp.$1
      , name: RegExp.$2
      , string: RegExp.$1 + '.prototype.' + RegExp.$2 + '()'
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.8"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>8 (str)](#apidoc.element.dox.contextPatternMatchers.8)
- description and source-code
```javascript
8 = function (str) {
  // prototype property
  if (/^\s*([\w$.]+)\s*\.\s*prototype\s*\.\s*([\w$]+)\s*=\s*([^\n;]+)/.exec(str)) {
    return {
        type: 'property'
      , constructor: RegExp.$1
      , cons: RegExp.$1
      , name: RegExp.$2
      , value: RegExp.$3.trim()
      , string: RegExp.$1 + '.prototype.' + RegExp.$2
    };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dox.contextPatternMatchers.9"></a>[function <span class="apidocSignatureSpan">dox.contextPatternMatchers.</span>9 (str)](#apidoc.element.dox.contextPatternMatchers.9)
- description and source-code
```javascript
9 = function (str) {
  // prototype property without assignment
  if (/^\s*([\w$]+)\s*\.\s*prototype\s*\.\s*([\w$]+)\s*/.exec(str)) {
    return {
        type: 'property'
      , constructor: RegExp.$1
      , cons: RegExp.$1
      , name: RegExp.$2
      , string: RegExp.$1 + '.prototype.' + RegExp.$2
    };
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dox.utils"></a>[module dox.utils](#apidoc.module.dox.utils)

#### <a name="apidoc.element.dox.utils.escape"></a>[function <span class="apidocSignatureSpan">dox.utils.</span>escape (html)](#apidoc.element.dox.utils.escape)
- description and source-code
```javascript
escape = function (html){
  return String(html)
    .replace(/&(?!\w+;)/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;');
}
```
- example usage
```shell
...
utils.js:

'''js
/**
* Escape the given 'html'.
*
* @example
*     utils.escape('<script></script>')
*     // => '&lt;script&gt;&lt;/script&gt;'
*
* @param {String} html string to be escaped
* @return {String} escaped html
* @api public
*/
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

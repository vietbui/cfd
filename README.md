# `cfd` - A wrapper for CloudFormation deploys

Easy CloudFormation deploys using only bash, jq and the aws cli

## Installation

    $ curl -L https://raw.githubusercontent.com/mgoodings/cfd/master/install.sh | bash

## Example

![](https://i.imgur.com/sjwSYkI.gif)

    $ cfd validate template.yml

    $ cfd plan example-stack template.yml params.json

    $ cfd apply example-stack template.yml params.json

    $ cfd tail example-stack

## Stack Parameters

Stack parameters can be injected using a JSON key/value file (optional) and/or by using prefixed environment variables (eg. CFVAR_ParameterName=ParameterValue)

## Usage

Output can also be obtained from `cfd --help`.

    Usage: cfd [options] [COMMAND] [args]

    Commands:

      cfd validate <template>                                            Validate a template
      cfd package <template> <output-template> <s3-bucket> <s3-prefix?>  Package a template for deployment
      cfd plan <stack> <template> <params?>                              Plan changes for a stack
      cfd apply <stack> <template> <params?>                             Apply changes to a stack
      cfd tail <stack>                                                   Tail latest stack events

    Options:

      -V, --version     Output current version of cfd
      -h, --help        Display help information
      -i, --ignore-env  Ignore CFVAR_ environment variables

    Aliases:

      v   validate
      k   package
      p   plan
      a   apply
      t   tail

## License

(The MIT License)

Copyright (c) 2018 Miles Goodings

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

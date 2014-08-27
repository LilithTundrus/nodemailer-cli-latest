# nodemailer-cli 0.0.1

A command line interface for sending email, wrapped around [nodemailer][nodemailer]. 

This module is not yet for public consumption: it was quickly assembled so I could easily send email from PresSTORE, and its interface mimics those requirements.

## Installation

Install the module globally to expose the `nodemailer` command to your environment.

```bash
npm install -g nodemailer-cli
```

## Usage

```
$ nodemailer --help

Usage: nodemailer <to> <from> <subject> <filename> [options]

to           Email address to send the mail to.
from         Email address that the message should be from.
subject      The string to be used as the email's subject.
filename     Path to the file to be used as the body of the email.

Options:
   -t, --service    The nodemailer service identifier, if any.
   -u, --username   The SMTP username to use when authenticating.  [local_user_name]
   -p, --password   The plain-text password to use when authenticating.
   -s, --server     The SMTP server that mail will be delivered to.
   -r, --port       The port to use when contacting the SMTP server.  [465]
   -n, --nossl      If set, SSL will not be used when sending mail.
```

## Environment Variables

Some environment variables can be used in place of CLI options.

- **SMTP_SERVER** The hostname of the SMTP server to be used.
- **SMTP_PORT** The port on the SMTP server that should be connected to.
- **SMTP_USERNAME** The username to use when authenticating.
- **SMTP_PASSWORD** The password to use when authenticating.
- **SMTP_USE_SSL** Set this to a truth-y value to use SSL.
- **SMTP_SERVICE_NAME** This is one of nodemailer's service identifiers, if you want it to configure itself automatically.


## History

- **v0.0.1**  
Initial Release



[nodemailer]: https://github.com/andris9/Nodemailer

## The MIT License (MIT)

Copyright (c) 2014 Nathan Wittstock

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

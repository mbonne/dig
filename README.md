# Collection of Domain and DNS checker scripts

## Purpose

Quick and easy way to run multiple dig checks against well known records for given domain.
As always cross check the results with other sources.
Ideally from the DNS admin portal for domain if you are the admin.

There will also be a short list of online resources to crosscheck results from. and some recommendations for how to improve domain security and reputation.

## Install

To install, add script file to your path for ease of use.

make a custom bin directory:
`mkdir -p $HOME/bin`

Add the following line to ~/.profile, ~/.bashrc, or ~/.zshrc

`export PATH=$HOME/bin:$PATH`

Symlink the script to custom bin folder:
`ln -s /Path/to/Github\ Folders/dig/digd $HOME/bin/digd`

Reload shell. Quit and reload terminal or use:
`source $HOME/.profile`

## Usage

digd example.com

## Example

output will look like this:

```shell
❯ digd example.com

>>> Domain Whois:
% IANA WHOIS server
% for more information on IANA, visit http://www.iana.org
% This query returned 1 object

domain:       EXAMPLE.COM

organisation: Internet Assigned Numbers Authority

created:      1992-01-01
source:       IANA


whois brief:
> Domain: example.com
> Name Servers:


Domain Lock State:
Disabled: clientTransferProhibited
Disabled: clientUpdateProhibited
Disabled: clientDeleteProhibited


>>> NS
a.iana-servers.net.
b.iana-servers.net.

DNSSEC:


>>> SOA
ns.icann.org. noc.dns.icann.org. 2024081420 7200 3600 1209600 3600

>>> A
93.184.215.14

>>> MX
0 .

>>> TXT
wgyf8z8cgvm2qmxpnbnldrcltvk4xqfn

SPF:
v=spf1 -all

Google DKIM:
v=DKIM1; p=


DMARC:
v=DMARC1;p=reject;sp=reject;adkim=s;aspf=s

>>> CNAME

>>> Zone Transfer Check
Checking a.iana-servers.net. for zone transfer...
Zone transfer failed on a.iana-servers.net. - This is good
Checking b.iana-servers.net. for zone transfer...
Zone transfer failed on b.iana-servers.net. - This is good

>>> End Domain Checks

```

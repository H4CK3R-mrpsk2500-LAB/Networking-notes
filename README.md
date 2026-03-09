# Networking-DNS-notes

## Topic: DNS

  DNS stands for Domain Name System 
  
  Its translate a website name into an ip address. so computers can find and connect to the correct server on the internet.
  Example:
  google.com ----> 142.250.183.14
  Humans remember domain names easily, but computers communicate using ip address.

## why DNS is used
  - Humans cannot remember ip addresses easily.
  - Domain names are easier to remember.
  - DNS helps locate the correct server on the internet.

## Types of DNS Server:

## 1.Recursive Resolver :
  A Recursive Resolver is the DNS server that receives the DNS query from the user and finds the correct IP address by asking other DNS         servers.
  Usage:
  It acts as a middleman between the user and DNS servers.
  It searches for the IP address step-by-step and returns the result to the user.

## 2.Root DNS Server :
  The Root DNS Server is the first level in the DNS hierarchy that receives queries from the recursive resolver.
  Usage:
  It does not store the IP address of websites.
  It only tells the resolver which Top-Level Domain (TLD) server to ask next.
    
## 3.TLD (Top-Level Domain) Server :
  The TLD server manages domain extensions such as:
  .com
  .org
  .net
  .edu
  Usage:
  It receives the request from the root server.
  It tells the resolver which Authoritative DNS server contains the final record.

## 4.Authoritative DNS Server :
  The Authoritative DNS Server is the final server that stores the actual DNS records and the real IP address of the domain.
  Usage:
  It provides the exact IP address of the website.
  This is the last step in DNS lookup.

 ## SIMPLE DNS QUERY FLOW:
  User
    ↓
  Recursive Resolver
    ↓
  Root DNS Server
    ↓
  TLD Server
    ↓
  Authoritative DNS Server
    ↓
  IP Address Returned


## DNS RECORD TYPES: 
  DNS records are entries in a DNS database that provide information about a domain, such as its IP address or mail server.

## 1.A Record (Address Record)
  An A record maps a domain name to an IPv4 address.
  Usage:
  It tells the browser which IPv4 address belongs to the domain.
  Example:
  google.com → 142.250.183.14
  This means when someone visits google.com, DNS returns this IPv4 address.

## 2.AAAA Record (IPv6 Address Record)
  An AAAA record maps a domain name to an IPv6 address.
  Usage:
  It is used when the website supports IPv6 networking.
  Example:
  google.com → 2001:0db8:85a3::8a2e:0370:7334

## 3.CNAME Record (Canonical Name Record)
  A CNAME record maps one domain name to another domain name.
  Usage:
  It is used to create aliases for domains.
  Example:
  www.example.com → example.com
  Here www.example.com⁠, points to example.com.

## 4.MX Record (Mail Exchange Record)
  An MX record specifies the mail server responsible for receiving emails for a domain.
  Usage:
  It is used in email services.
  Example:
  example.com → mail.example.com
  This tells email servers where to deliver messages.

## 5.NS Record (Name Server Record)
  An NS record specifies which DNS server is responsible for a domain.
  Usage:
  It helps the internet know which DNS server contains the domain information.
  Example:
  example.com → ns1.exampledns.com

## 6.TXT Record (Text Record)
  A TXT record stores text information in DNS.
  Usage:
  It is mainly used for security verification and email authentication.
  Example uses:
  SPF (Sender Policy Framework)
  Domain verification
  Email security
  Example:
  v=spf1 include:_spf.google.com
  
  
  

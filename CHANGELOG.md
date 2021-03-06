# Changelog


## Release 1.2.0

- NEW: Allow a custom List on `PublicSuffix.parse` (GH-26). [Thanks @itspriddle]

- FIXED: PublicSuffix.parse and PublicSuffix.valid? crashes when input is nil (GH-20).

- CHANGED: Updated definitions.


## Release 1.1.3

- CHANGED: Updated definitions.


## Release 1.1.2

- CHANGED: Updated definitions.


## Release 1.1.1

- CHANGED: Updated definitions.


## Release 1.1.0

- FIXED: #valid? and #parse consider URIs as valid domains (GH-15)

- CHANGED: Updated definitions.

- CHANGED: Removed deprecatd PublicSuffixService::RuleList.


## Release 1.0.0

- CHANGED: Updated definitions.


## Release 1.0.0.rc1

The library is now known as PublicSuffix.


## Release 0.9.1

- CHANGED: Renamed PublicSuffixService::RuleList to PublicSuffixService::List.

- CHANGED: Renamed PublicSuffixService::List#list to PublicSuffixService::List#rules.

- CHANGED: Renamed PublicSuffixService to PublicSuffix.

- CHANGED: Updated definitions.


## Release 0.9.0

- CHANGED: Minimum Ruby version increased to Ruby 1.8.7.

- CHANGED: rake/gempackagetask is deprecated.  Use rubygems/package_task instead.


## Release 0.8.4

- FIXED: Reverted bugfix for issue #12 for Ruby 1.8.6.
  This is the latest version compatible with Ruby 1.8.6.


## Release 0.8.3

- FIXED: Fixed ArgumentError: invalid byte sequence in US-ASCII with Ruby 1.9.2 (#12).

- CHANGED: Updated definitions (#11).

- CHANGED: Renamed definitions.txt to definitions.dat.


## Release 0.8.2

- NEW: Added support for rubygems-test.

- CHANGED: Integrated Bundler.

- CHANGED: Updated definitions.


## Release 0.8.1

- FIXED: The files in the release 0.8.0 have wrong permission 600 and can't be loaded (#10).


## Release 0.8.0

- CHANGED: Update public suffix list to d1a5599b49fa 2010-10-25 15:10 +0100 (#9)

- NEW: Add support for Fully Qualified Domain Names (#7)


## Release 0.7.0

- CHANGED: Using YARD to document the code instead of RDoc.

- FIXED: RuleList cache is not recreated when a new rule is appended to the list (#6)

- FIXED: PublicSuffixService.valid? should return false if the domain is not defined or not allowed (#4, #5)


## Release 0.6.0

- NEW:  PublicSuffixService.parse raises DomainNotAllowed when trying to parse a domain name
  which exists, but is not allowed by the current definition list (#3)

        PublicSuffixService.parse("nic.do")
        # => PublicSuffixService::DomainNotAllowed

- CHANGED: Renamed PublicSuffixService::InvalidDomain to PublicSuffixService::DomainInvalid


## Release 0.5.2

- CHANGED: Update public suffix list to 248ea690d671 2010-09-16 18:02 +0100


## Release 0.5.1

- CHANGED: Update public suffix list to 14dc66dd53c1 2010-09-15 17:09 +0100


## Release 0.5.0

- CHANGED: Improve documentation for Domain#domain and Domain#subdomain (#1).

- CHANGED: Performance improvements (#2).


## Release 0.4.0

- CHANGED: Rename library from DomainName to PublicSuffixService to reduce the probability of name conflicts.


## Release 0.3.1

- Deprecated DomainName library.


## Release 0.3.0

- CHANGED: DomainName#domain and DomainName#subdomain are no longer alias of Domain#sld and Domain#tld.

- CHANGED: Removed DomainName#labels and decoupled Rule from DomainName.

- CHANGED: DomainName#valid? no longer instantiates new DomainName objects. This means less overhead.

- CHANGED: Refactoring the entire DomainName API. Removed the internal on-the-fly parsing. Added a bunch of new methods to check and validate the DomainName.


## Release 0.2.0

- NEW: DomainName#valid?

- NEW: DomainName#parse and DomainName#parse!

- NEW: DomainName#valid_domain? and DomainName#valid_subdomain?

- CHANGED: Make sure RuleList lookup is only performed once.


## Release 0.1.0

- Initial version

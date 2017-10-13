## Rules and Guidelines for AL Code ##

This page defines the rules and guidelines to follow when writing AL code in an extension package. The rules and guidelines are grouped according to two importance levels: Critical errors that must be resolved, and important errors that should be resolved. Errors that are not resolved must include an explanation and justification for the error.

### Critical Errors ###

- Code uses NAV encryption key functions, IMPORTENCRYPTIONKEY, EXPORTENCRYPTIONKEY, CREATEENCRYPTIONKEY, DELETEENCRYPTIONKEY. (FYI - It is fine to use the ENCRYPT and DECRYPT functions.)
- Code uses ASSERTERROR
- External data connections do not properly handle sensitive data
- Code uses AutoIncrement=Yes for a table field that may be used in a Foreign Key relationship. Recommend code comment that the table field will not be used in a Foreign Key relationship to pass validation
- Doesn’t encrypt sensitive table data. (i.e. credit card info, passwords, etc.)

### Important Errors ###

- Temporary files are not cleaned up after use
- Code uses codeunits that require printers to be selected
- Code uses a specific time zone or locale
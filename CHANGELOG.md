## Changelog

All changes are in the `main` branch (`master` remains unchanged).

### v3.3.0

+   `NameID` format can be passed as a parameter to `esaml_sp:generate_authn_request/3`.
    Deprecated `esaml_sp:generate_authn_request/2`. Pass in `undefined` as NameID format
    if you do not want to pass in `NameIDPolicy` in the authn request.

+   Passing `#esaml_subject{}` with the values returned in the authn response
    assertion subject. This is essential for sending appropriate `NameQualifier`,
    `SPNameQualifier` and `Format` values in the SLO logout request. Without these
    values, Shibboleth fails to match the SP session on the IdP side. Deprecated
    `esaml_sp:generate_logout_request/3`. It will be removed in a future relase.

### v3.2.0

+   Generate SP Metadata XML that passes schema validation

### v3.1.0

+   Support for customizable SP entity_id
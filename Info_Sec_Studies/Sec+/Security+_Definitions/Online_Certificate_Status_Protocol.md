Sources:
https://www.ibm.com/docs/api/v1/content/ssw_ibm_i_71/rzain/rzainocsp.htm
\
[[OCSP]] provides applications a way to determine the revocation status for a digital [[Certificate]]. [[Certificate]] revocation status that is checked via [[OCSP]] provides more up-to-date status information than is available through [[CRL]]s.
\
The implementation of [[OCSP]] revocation status checking is done in accordance with RFC 2560. [[OCSP]] certificate revocation status checking is available for the end entity certificate. Protocol version 1 over [[HTTP]] and the basic response type are supported.
\
Certificate revocation status is checked by an application via [[OCSP]] when at least one of the following conditions are true:

-   A [[URL]] address of an [[OCSP]] responder is configured.
-   Authority Information Access ([[AIA]]) checking is enabled and the certificate to be validated has an [[AIA]] extension. The [[AIA]] extension must contain a PKIK_AD_OCSP access method with a [[URI]] that indicates the [[HTTP]] location of the [[OCSP]] responder.

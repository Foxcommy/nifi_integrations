How to solve ssl issue.

Full description of error is the following:

InvokeHTTP[id=3df95e30-0180-1000-0000-000020a5c621] Routing to Failure due to exception: sun.security.validator.ValidatorException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target: javax.net.ssl.SSLHandshakeException: sun.security.validator.ValidatorException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target

We can get this error while trying to execute invokehttp without a valid certificate. The solition is pretty simple we need to export certificate via openssl tool and than add this certificate to the truststore. Export and import commands is available in the sss_issue folder.

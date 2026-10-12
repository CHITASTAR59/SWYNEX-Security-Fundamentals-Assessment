# Security Fundamentals Assessment

## 1. Executive Summary

An initial security assessment was performed against OWASP
Juice Shop running in a local Ubuntu Docker environment.

The work covered HTTP response headers and frontend routing
behavior for an unknown application path.

The initial tests did not establish a confirmed vulnerability.
Authentication, session security, and access-control testing
remain to be completed.

## 2. Scope

Target:
http://127.0.0.1:3000

Environment:
Ubuntu, Docker, OWASP Juice Shop.

Testing was restricted to the local training application.

## 3. Methodology

- Inspected HTTP response headers using curl.
- Reviewed a request in Firefox Developer Tools.
- Requested a nonexistent frontend path.
- Compared the unknown-path response with the homepage.
- Documented observations and potential areas for further review.

## 4. Findings and Observations

### SF-001: HTTP Security Header Review

Status: Informational; further assessment required.

Evidence:
../evidence/http-headers.txt

Observed:
- X-Content-Type-Options: nosniff
- X-Frame-Options: SAMEORIGIN
- Access-Control-Allow-Origin: *

The first two headers are positive security observations.
The wildcard CORS policy requires evaluation against the
resource's sensitivity and intended cross-origin access.

The captured evidence does not establish a confirmed CORS
vulnerability.

Recommendation:
Review CORS policies for sensitive resources and verify
the intended security-header configuration.

### SF-002: Unknown Frontend Route

Status: No vulnerability established.

Test:
Requested /swynex-assessment-test.

Observed:
HTTP status 200.

The response body matched the homepage response body.
This behavior is consistent with a single-page application
serving its frontend shell for unknown routes.

The test did not establish an error-handling vulnerability.

Recommendation:
Assess backend error handling separately if it is within
the authorized lab scope.

## 5. Assessment Limitations

Authentication, session management, and access-control
testing have not yet been documented as completed.

No claims are made that these controls are vulnerable.

## 6. Conclusion

The initial assessment documented HTTP response behavior
and identified security configuration areas for further review.

Additional testing and evidence are required before
classifying any issue as a confirmed vulnerability.

## 7. Responsible Testing

All testing was limited to the locally hosted training
application.

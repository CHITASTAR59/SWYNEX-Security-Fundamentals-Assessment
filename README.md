# SWYNEX Security Fundamentals Assessment

## Overview

This project documents a web application security assessment
conducted against an intentionally vulnerable application in
a controlled local lab environment.

## Objectives

- Review HTTP security headers.
- Examine error handling.
- Review authentication and session security.
- Understand access-control requirements.
- Document evidence and remediation recommendations.

## Lab Environment

- Operating system: Ubuntu
- Application: OWASP Juice Shop
- Deployment: Local Docker container
- Target: http://127.0.0.1:3000

## Repository Structure

- `report/`: Assessment reports and findings.
- `evidence/`: Sanitized evidence collected during testing.
- `remediation/`: Recommended corrective measures.

## Methodology

The assessment uses manual inspection of HTTP responses,
browser-based review, and controlled tests within the local
training application.

## Findings

Only verified findings will be classified as confirmed
vulnerabilities. Observations requiring further validation
will be identified separately.

## Responsible Testing

All testing is limited to the local training environment.
No external systems are included in the assessment.


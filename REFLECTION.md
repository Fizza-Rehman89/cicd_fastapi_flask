# CI/CD Pipeline Reflection

## What does each stage protect against?
- **Lint:** Protects against poor code formatting and style issues that make 
  code harder to read and maintain.
- **Test:** Protects against bugs and broken functionality by verifying that 
  all endpoints behave as expected.
- **Deploy:** Ensures only verified, tested code reaches production, protecting 
  end users from broken releases.

## Why does order matter?
If deploy ran before test, broken code could reach production and affect real 
users. The pipeline enforces order so that deployment only happens after all 
quality checks pass.

## One improvement for production?
Add environment-specific secrets and real deployment to a cloud platform like 
Render or Railway, instead of a simulated echo command.
# Black Duck CoPilot Rubygems/Circle CI Example

[![CircleCI](https://circleci.com/gh/BlackDuckCoPilot/example-rubygems-circle/tree/master.svg?style=svg)](https://circleci.com/gh/BlackDuckCoPilot/example-rubygems-circle/tree/master) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-rubygems-circle/branches/master/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-rubygems-circle/branches/master)

Shows a working setup for using Black Duck CoPilot to analyze the risk of project dependencies

# Circle CI Setup
The `circle.yml` file has been modified to upload the generated data to Black Duck CoPilot:
```yaml
test:
  post:
    - bash <(curl -s https://copilot.blackducksoftware.com/ci/circle/scripts/upload)
```

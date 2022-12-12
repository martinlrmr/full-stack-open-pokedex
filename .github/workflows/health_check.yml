on:
  schedule:
    - cron: '15,30,45,00 0-23 * * 0-6'

jobs:
  test_schedule:
    runs-on: ubuntu-latest
    steps:
  - name: Check the deployed service URL
    uses: jtalk/url-health-check-action@v3
    with:
      # Check the following URLs one by one sequentially
      url: https://fullstack-cicd.fly.dev/health|https://fullstack-cicd.fly.dev/
      # Follow redirects, or just report success on 3xx status codes
      follow-redirect: false # Optional, defaults to "false"
      # Fail this action after this many failed attempts
      max-attempts: 3 # Optional, defaults to 1
      # Delay between retries
      retry-delay: 5s # Optional, only applicable to max-attempts > 1
      # Retry all errors, including 404. This option might trigger curl upgrade.
      retry-all: false # Optional, defaults to "false"
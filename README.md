# SonarQube Scan Action

Run SonarQube scans and enforce the Quality Gate.

## Inputs

- `project_key` (required) — SonarQube project key
- `sonar_host` (required) — SonarQube URL
- `sonar_token` (required) — SonarQube token (use secrets)

## Example

```yaml
jobs:
  sonar:
    runs-on: ubuntu-latest
    steps:
      - name: Run Sonar Scan
        uses: chetanbothra/sonarqube-scan-action@v1
        with:
          project_key: my-service
          sonar_host: ${{ secrets.SONARQUBE_HOST }}
          sonar_token: ${{ secrets.SONARQUBE_TOKEN }}

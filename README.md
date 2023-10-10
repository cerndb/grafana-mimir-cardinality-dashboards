# grafana-mimir-cardinality-dashboards
Grafana Mimir dashboards used for cardinality exploration

## Requirements
- Grafana v8.5+
- JSON API datasource: https://grafana.com/grafana/plugins/marcusolsson-json-datasource/
- TreeMap panel: https://grafana.com/grafana/plugins/marcusolsson-treemap-panel/

## Usage
You can import the dashboards using Grafana GUI, in order for them to work you will need to have configured:
- A JSON API datasource pointing to your cardinality endpoint: https://<host>/prometheus/api/v1/cardinality/
- A multi-tenancy deployment for Grafana Mimir and proper ACLs configured

Dashboards are configured to set the X-Scope-OrgId  from a "tenant" variable that needs to be configured in the dashboard so it can be selected dynamically.

## Disclaimer
These dashboard are mainly for internal usage and fully based on the ones found in https://play.grafana.org/,
and are being shared here as a request from different people from the community.

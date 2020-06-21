# AG kusama-grafana-dashboard
## based on [polkadot metrics](https://grafana.com/grafana/dashboards/11171) dashboard
1. `polkadot --chain kusama --prometheus-external`
2. add job named `kusama` to `prometheus.yml`:
```
  - job_name: kusama
    static_configs:
      - targets: ['Kusama1-Validator.host.com:9615', 'Kusama1-Sentry.host2.com:9615']

```
3. import json
4. add notification channels to `block Sync rate [5m]` and `Number of network sync peers` panels
5. if prometheus job is named not `kusama` (`polkadot` for example) then go to Settings\Variables and change `$job`

![screenshot](https://github.com/AGx10k/kusama-grafana-dashboard/blob/master/kusama-dashboard-screeenshot.PNG?raw=true)

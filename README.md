# WxPlatformInsight4PE

This project provides Prometheus metrics on Process Engine (PE) assets.

## Related Work

* [WxPrometheus](https://github.com/IBM/WxPrometheus)
* [WxPlatformMonitoring](https://github.com/IBM/WxPlatformMonitoring)

## Dependencies 

Following dependent packages must be also installed ...

* [WxPrometheus](https://github.com/IBM/WxPrometheus)
* [WxPlatformMonitoring](https://github.com/IBM/WxPlatformMonitoring)

## Version History

### v1.0.0

This package is optional and provides metrics of process which are running inside Process Engine. To provide the metrics, the monitoring service `pub.monitor.process.model:getModelList` is called. The metrics `sag_pe_processes_completed`, `sag_pe_processes_failed` and `sag_pe_processes_started` can be scrapped.

*Tipp:* See the [webMethods Dashboard](./dashboards/webMethods.json) and use the `rate()` function to get the wanted monitoring signal. 

### v1.1.0

Following metrics are added to detect non activities on process instances. The metrics are only printed for started processes:

* `sag_pe_process_non_activity_duration_time`: Time duration since last activity.
* `sag_pe_process_running_duration_time`: Time duraton since process intstance was started.

### v1.2.0

Started and failed processes are printed in `sag_pe_process_non_activity_duration_time` and `sag_pe_process_running_duration_time`. Additional, a label `status` is added. The process instance status is written to this label.

### v1.2

Same version as `v1.2.0`. Switch version numbering from 3 digits to 2.

## Disclaimer

### IBM Public Repository Disclosure

All content in these repositories including code has been provided by IBM under the associated open source software license and IBM is under no obligation to provide enhancements, updates, or support. IBM developers produced this code as an open source project (not as an IBM product), and IBM makes no assertions as to the level of quality nor security, and will not be maintaining this code going forward.
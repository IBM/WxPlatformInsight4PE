# WxPlatformInsight4PE

This project provides Prometheus metrics on Process Engine (PE) assets.

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

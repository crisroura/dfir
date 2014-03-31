dfir
====

Digital Forensics and Incident Response Scripts


pe_compile_ts_anomalies.py
--------------------------
This script checks the compilation timestamp from pe files. Creates a csv output with: the name of the file, the compilation timestamp and a value indicating if the timestamp is normal or anomalous. Compilation timestamps are in UTC.

This script is based on pescanner.py (Michael Ligh) to check only compilation timestamps and use it in the triage of malware incidents.

#### Usage example ####
```shell
$ python pe_compile_ts_anomalies.py /mnt/windows_mount/Windows/System32/
filename,timestamp(M/D/Y H:M:S),timezone,anomaly
/mnt/windows_mount/Windows/System32/aaclient.dll,07/14/2009 01:03:45,UTC,normal
/mnt/windows_mount/Windows/System32/accessibilitycpl.dll,07/14/2009 01:03:52,UTC,normal
...
/mnt/windows_mount/Windows/System32/zh-TW/msimsg.dll.mui,07/13/2009 23:31:14,UTC,normal
/mnt/windows_mount/Windows/System32/zh-TW/msprivs.dll.mui,07/13/2009 23:33:53,UTC,normal

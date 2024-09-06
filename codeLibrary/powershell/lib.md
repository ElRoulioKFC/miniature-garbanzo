kill process
```pwsh
taskkill.exe /PID <PID> /F

```

find process using port
```pwsh
netstat -ano | findstr <port>

```

find in history this regex
```pwsh
Get-Content (Get-PSReadlineOption).HistorySavePath | ? { $_ -like '<regex>' }

```
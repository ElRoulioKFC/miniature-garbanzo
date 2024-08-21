kill process
```pwsh
taskkill.exe /PID {PID} /F

```

find process using port {port}
```pwsh
netstat -ano | findstr {port}

```

find in history this regex {reg}
```pwsh
Get-Content (Get-PSReadlineOption).HistorySavePath | ? { $_ -like '{reg}' }

```
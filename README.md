# Notepad-Installer-via-PowerShell

  Write-Host "Downloading Notepad++ installer..."
$installerPath = "C:\Users\shaaf\Downloads\npp.8.1.9.3.Installer.exe"
Invoke-WebRequest -Uri "https://github.com/notepad-plus-plus/notepad-plus-plus/releases/download/v8.1.9.3/npp.8.1.9.3.Installer.exe" -OutFile $installerPath

Write-Host "Running Notepad++ installer..."
Start-Process -FilePath $installerPath -ArgumentList "/S" -Wait

Write-Host "Notepad++ installation completed."

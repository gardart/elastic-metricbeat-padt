# elastic-metricbeat-padt
Elastic Metricbeat deployment package for Windows

# Installation
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-WebRequest -Uri "https://github.com/gardart/elastic-metricbeat-padt/archive/master.zip" -outfile "$env:TEMP\master.zip" -Verbose
Expand-Archive -Path "$env:TEMP\master.zip" -DestinationPath "$env:TEMP" -Force -Verbose
. $env:TEMP\elastic-metricbeat-padt-master\Deploy-Application.ps1

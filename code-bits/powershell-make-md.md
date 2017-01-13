5..100 | % { New-Item -Path d:\2sort -Name “$_.md” -Value (Get-Date).toString() -ItemType file}

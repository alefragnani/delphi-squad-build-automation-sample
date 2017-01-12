# Jenkins Notes

## Compila��o B�sica

1. Gerenciamento de c�digo fonte / Git / Repository URL: 

  `file:///`

2. Trigger de Builds / Consultar Periodicamente o SCM: 

  `*/1 * * * *`

3. Build / Executar Comando no Windows: 

  `"D:\program files\FinalBuilder 8\FBCMD.exe" /p"%WORKSPACE%\Squad.fbp8"`

4. A��es P�s Build / Arquivar os Artefados: 

  `Artifacts/Build.zip`

## Compila��o com DUnit

1. A��es P�s Build / Publish NUnit report:

  `Artifacts/dunit-report.xml`

## Compila��o com Code Coverage

1. A��es P�s Build / Record emma:

  `Artifacts/Coverage/CodeCoverage_Summary.xml`


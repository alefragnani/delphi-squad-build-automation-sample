# Jenkins

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

# FinalBuilder

## Compila��o B�sica

1. Compilar Delphi:

  `%FBPROJECTDIR%\src\Project1.dpr`

2. Criar pasta Artefatos:

  `%FBPROJECTDIR%\Artifacts`

3. Copiar exe para Artefatos:

  `%FBPROJECTDIR%\Bin\*.exe -> %FBPROJECTDIR%\Artifacts`

4. Compactar Artefatos:

  `%FBPROJECTDIR%\Artifacts\Build.zip` Files: `*.*`

## Compila��o com DUnit

1. Compilar Delphi:

  `%FBPROJECTDIR%\tests\Project1Tests.dpr` 

2. Executar Testes (Start In)

  `"%FBPROJECTDIR%\Bin\Project1Tests.exe"` // aspas duplas

3. Copiar relat�rio para Artefatos:

  `%FBPROJECTDIR%\Bin\dunit-report.xml -> %FBPROJECTDIR%\Artifacts`

## Compila��o com Code Coverage

1. Criar pasta Coverage:

  `%FBPROJECTDIR%\Bin\Coverage`

2. Criar BAT do Coverage
  
  `%FBPROJECTDIR%\Bin\cc.bat`
  `"%FBPROJECTDIR%\Coverage\CodeCoverage.exe" -e "%FBPROJECTDIR%\Bin\Project1Tests.exe" -m "%FBPROJECTDIR%\Bin\Project1Tests.map" -sd "%FBPROJECTDIR%\src" -u uCalculadora.pas -html -emma -xml -od "%FBPROJECTDIR%\Bin\Coverage"`

3. Executar BAT do Coverage

  `"%FBPROJECTDIR%\Bin\cc.bat"`

4. Copiar relat�rio para Artefatos:

  `%FBPROJECTDIR%\Bin\Coverage\*.* -> %FBPROJECTDIR%\Artifacts\Coverage`

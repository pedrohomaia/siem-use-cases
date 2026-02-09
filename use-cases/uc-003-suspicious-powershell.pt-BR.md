# Use Case SIEM — Execução suspeita de PowerShell

## Objetivo de detecção
Identificar padrões incomuns de execução de PowerShell em endpoints.

## Fontes de log
- Windows (Security/Sysmon se existir)
- EDR telemetry

## Lógica (alto nível)
- PowerShell com parâmetros incomuns para o ambiente
- Execução por usuário não típico
- Frequência anormal em curto período

## Tuning / falsos positivos
- Scripts legítimos de TI
- Ferramentas de automação corporativa

## Passos de investigação
- Verificar usuário, host, comando e cadeia de processos
- Correlacionar com downloads, conexões e persistência

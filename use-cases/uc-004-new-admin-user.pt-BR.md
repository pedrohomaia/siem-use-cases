# Use Case SIEM — Criação de usuário admin / elevação de privilégio

## Objetivo de detecção
Detectar criação de conta privilegiada ou elevação de permissão.

## Fontes de log
- Windows Security (eventos de grupos/contas)
- Logs do IAM/IdP

## Lógica (alto nível)
- Evento de adição a grupo privilegiado
- Criação de conta com role admin

## Tuning / falsos positivos
- Janelas de mudança (change window)
- Ações de equipe de IAM (whitelist controlada)

## Passos de investigação
- Confirmar change request
- Verificar autor, host e horário
- Checar atividades após elevação

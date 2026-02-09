# Use Case SIEM — Múltiplas falhas de logon (spray / password guessing)

## Objetivo de detecção
Detectar múltiplas falhas distribuídas em vários usuários a partir de uma origem.

## Fontes de log
- Auth logs
- IdP/SSO

## Lógica (alto nível)
- Muitas falhas para vários usuários em X minutos
- Mesma origem (IP/ASN)

## Tuning / falsos positivos
- Sistemas mal configurados
- Testes internos (registrar e limitar)

## Passos de investigação
- Identificar lista de contas alvo
- Verificar se houve sucessos
- Ações de contenção e reset/mfa

# Use Case SIEM — Tentativa de brute force em autenticação

## Objetivo de detecção
Detectar múltiplas falhas de login em curto período para o mesmo usuário/IP.

## Fontes de log
- Auth logs (Windows Security / Linux auth)
- IdP/SSO logs (se houver)

## Lógica (alto nível)
- N falhas em X minutos para o mesmo usuário ou origem
- Opcional: correlação com sucesso posterior

## Tuning / falsos positivos
- Sistemas com usuários compartilhados/robôs
- Ajustar thresholds e whitelists

## Passos de investigação
- Verificar origem, geolocalização (se aplicável), horários
- Confirmar se houve sucesso após falhas
- Checar se usuário reportou problemas

# Use Case SIEM — DNS para domínio novo/raramente visto

## Objetivo de detecção
Detectar endpoints consultando domínios recém-registrados ou raros.

## Fontes de log
- DNS logs / Secure DNS
- Proxy logs

## Lógica (alto nível)
- Domínio com baixa prevalência no ambiente
- Acesso repetido por um host em janela curta

## Tuning / falsos positivos
- Ferramentas SaaS novas
- Atualizações/telemetria legítima

## Passos de investigação
- Verificar processo no endpoint associado à conexão (se disponível)
- Conferir reputação e contexto do usuário/host

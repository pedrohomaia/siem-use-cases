# Use Case SIEM — Impossible Travel

## Objetivo de detecção
Detectar logins do mesmo usuário em localizações incompatíveis em curto intervalo.

## Fontes de log
- IdP/SSO logs (Azure AD/Okta/etc.)
- VPN logs (se houver)

## Lógica (alto nível)
- Dois logins bem-sucedidos para o mesmo usuário
- Distância/tempo incompatíveis (janela curta)

## Tuning / falsos positivos
- VPN corporativa mudando egress IP
- Dispositivos mobile alternando redes

## Passos de investigação
- Checar device, ASN, IP e histórico do usuário
- Confirmar com usuário e revisar ações pós-login

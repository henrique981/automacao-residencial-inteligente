# JWT - JSON Web Token
Data: 2026-06-26
Status: Concluido e Testado

## O que e JWT?

JWT = JSON Web Token
E um "cracha digital" que prova quem voce e!

Sem JWT: qualquer um acessa sua API
Com JWT: so quem tem token valido acessa!

## Estrutura do JWT

Um JWT tem 3 partes separadas por ponto:

xxxxx.yyyyy.zzzzz
  |      |      |
  |      |      Assinatura
  |      Payload (dados)
  Header (tipo)

## Exemplo Gerado

Token criado no JWT.io:
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJFU1AzMl9zYWxhIiwiZGlzcG9zaXRpdm8iOiJFU1AzMl8wMDEiLCJyb2xlIjoic2Vuc29yIiwiYW1iaWVudGUiOiJzYWxhIiwiZXhwIjoxNzM1Nzc2MDAwfQ.Nv-4jZ-qqCLWqowse-6KP7KC-G-qNwzlXsXpveob9G4

## Header

{
  "alg": "HS256",
  "typ": "JWT"
}

alg = algoritmo de criptografia (HS256)
typ = tipo do token (JWT)

## Payload

{
  "sub": "ESP32_sala",
  "dispositivo": "ESP32_001",
  "role": "sensor",
  "ambiente": "sala",
  "exp": 1735776000
}

sub = subject (quem e o dispositivo)
role = papel (sensor, admin, user)
ambiente = onde esta o ESP32
exp = quando o token expira

## Testes Realizados

- Token criado com JWT Encoder
- Token decodificado com JWT Decoder
- Chave correta = Signature Verified
- Chave errada = Invalid Signature
- Alteracao no payload = token invalido

## Como Funciona no Projeto

1. ESP32 faz login com device_id + secret
2. Servidor valida e gera JWT
3. ESP32 usa JWT em cada request
4. Servidor valida JWT
5. JWT expirado = faz login de novo

## Seguranca Implementada

- Algoritmo HS256
- Chave secreta forte
- Token com expiracao
- Assinatura verificada

## Ferramentas Usadas

- JWT.io (criar e validar tokens)
- JWT Encoder (criar tokens)
- JWT Decoder (verificar tokens)

## Proximos Passos

- Implementar JWT no codigo ESP32
- Integrar JWT com MQTT
- Adicionar refresh token

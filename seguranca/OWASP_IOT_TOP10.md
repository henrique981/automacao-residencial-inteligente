# Seguranca IoT - OWASP IoT Top 10
Data: 2026-06-24
Autor: Henry - Especialista IoT Security

## Vulnerabilidades e Solucoes

### I1 - Senhas Fracas
Risco: ALTO
Solucao: Senha forte no MQTT e Home Assistant

### I2 - Servicos Desnecessarios
Risco: MEDIO
Solucao: Fechar portas nao utilizadas

### I3 - Interfaces Inseguras
Risco: ALTO
Solucao: JWT em todas as APIs + HTTPS

### I4 - Falta de Atualizacao
Risco: MEDIO
Solucao: OTA (Over The Air) no ESP32

### I5 - Componentes Inseguros
Risco: MEDIO
Solucao: Atualizar bibliotecas regularmente

### I6 - Privacidade Insuficiente
Risco: ALTO
Solucao: Criptografia + conformidade LGPD

### I7 - Transferencia Insegura
Risco: ALTO
Solucao: MQTT com TLS/SSL (porta 8883)

### I8 - Sem Gerenciamento
Risco: MEDIO
Solucao: Inventario e monitoramento de dispositivos

### I9 - Configuracoes Padrao
Risco: ALTO
Solucao: Forcar troca de senha no primeiro acesso

### I10 - Seguranca Fisica
Risco: MEDIO
Solucao: ESP32 em local seguro com logs de acesso

## Proximos Passos
1. Implementar MQTT com TLS
2. Adicionar JWT nas APIs
3. Configurar OTA no ESP32
4. Criar dashboard de monitoramento

# Documentacao Tecnica - Servo SG90
Data: 2026-06-24
Status: Completo

## Componentes
- Servo SG90 (D5) - Motor de Posicionamento
- Resistor 220 ohm - Protecao

## Pinos
- V+ = 5V
- GND = GND
- PWM = D5 (via resistor 220 ohm)

## Como Funciona
- Pulso 1000 us = 0 graus
- Pulso 1500 us = 90 graus
- Pulso 2000 us = 180 graus
- Frequencia: 50 Hz (20ms periodo)

## Testes
- Movimento 0 a 180 graus OK
- Movimento 180 a 0 graus OK
- Posicoes especificas OK (45, 90, 135)
- Gradiente suave funcionando

## Aplicacoes
- Cortinas automaticas
- Trancas inteligentes
- Ventilacao automatica

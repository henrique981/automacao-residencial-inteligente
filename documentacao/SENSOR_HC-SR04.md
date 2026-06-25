# Documentacao Tecnica - HC-SR04 Ultrassonico
Data: 2026-06-24
Status: Completo

## Componentes
- HC-SR04 (TRIG D5, ECHO D18) - Sensor de Distancia

## Como Funciona
- Emite onda sonora 40kHz
- Mede tempo de retorno
- Formula: distancia (cm) = duracao (us) / 58

## Pinos
- TRIG = D5 (envia pulso 10us)
- ECHO = D18 (recebe retorno)
- VCC = 5V
- GND = GND

## Testes
- Tempo: 4530 us
- Distancia: 78.10 cm
- Funcionando corretamente

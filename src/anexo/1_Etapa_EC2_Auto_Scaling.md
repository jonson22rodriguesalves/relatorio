* GFT Start 7 Boot Camp 2025

# EC2 Auto Scaling - Implementação Pague Menos
**Data:** 04/08/2025  
**Responsável:** Jonson Rodrigues Alves

## **1. Visão Geral**
O **EC2 Auto Scaling** é um serviço AWS que ajusta automaticamente o número de instâncias EC2 com base na demanda, 
garantindo custos otimizados e alta disponibilidade.

## **2. Configuração Implementada**
### **2.1. Parâmetros Principais**
```yaml
AutoScalingGroup:
  MinSize: 2
  MaxSize: 10
  DesiredCapacity: 4
  HealthCheckType: EC2
  ScalingPolicies:
    - TargetTrackingConfiguration:
        Metric: CPUUtilization
        TargetValue: 70%

Gatilhos de Escalonamento
Scale-Out: Acionado quando CPU > 70% por 5 minutos.

Scale-In: Acionado quando CPU < 30% por 15 minutos.

3. Caso de Uso na Pague Menos
3.1. Problema Identificado
Picos de tráfego durante promoções causavam lentidão.

Instâncias ociosas geravam custos desnecessários fora de picos.

3.2. Solução
Implantação de grupos de Auto Scaling com políticas baseadas em métricas de CPU.

Uso de Amazon Machine Images (AMIs) pré-configuradas para rápida implantação.

4. Vantagens
✔ Redução de 30% nos custos com infraestrutura.
✔ Disponibilidade contínua mesmo sob tráfego intenso.
✔ Integração com CloudWatch para monitoramento automatizado.

5. Próximas Melhorias
Migrar para Spot Instances para economias adicionais.

Implementar Load Balancer para distribuição avançada.

Assinatura: Jonson Rodrigues Alves
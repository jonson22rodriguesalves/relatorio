* GFT Start 7 Boot Camp 2025

---

### **Arquivo 3: `anexo/rds_aurora_serverless.md`**
```markdown
# RDS Aurora Serverless - Implementação Pague Menos  
**Data:** 04/08/2025  
**Responsável:** Jonson Rodrigues Alves  

## **1. Visão Geral**  
O **Amazon Aurora Serverless** é um banco de dados relacional que escala automaticamente,
eliminando a necessidade de provisionamento manual.  

## **2. Configuração Implementada**  
### **2.1. Parâmetros do Cluster**  
```yaml
DBCluster:
  Engine: aurora-postgresql
  CapacityUnits:
    Min: 2
    Max: 16
  AutoPause: true
  TimeoutInactive: 300s

Escalonamento Automático
Aumento de capacidade: Acionado quando conexões > 80%.

Redução de capacidade: Ocorre após 5 minutos de inatividade.

3. Caso de Uso na Pague Menos
3.1. Problema Identificado
Bancos de dados provisionados estavam ociosos 60% do tempo.

Custos fixos altos mesmo em períodos de baixa demanda.

3.2. Solução
Migração de 5 bancos de dados para Aurora Serverless.

Configuração de auto-pause após inatividade.

4. Vantagens
✔ Redução de 70% nos custos com banco de dados.
✔ Escalonamento sob demanda sem intervenção manual.
✔ Compatibilidade com PostgreSQL/MySQL.

5. Próximas Melhorias
Implementar leitura distribuída para melhor performance.

Integrar com AWS Lambda para processamento de dados.

Assinatura: Jonson Rodrigues Alves
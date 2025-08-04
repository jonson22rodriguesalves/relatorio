* GFT Start 7 Boot Camp 2025

---

### **Arquivo 2: `anexo/s3_intelligent_tiering.md`**
```markdown
# S3 Intelligent-Tiering - Implementação Pague Menos  
**Data:** 04/08/2025  
**Responsável:** Jonson Rodrigues Alves  

## **1. Visão Geral**  
O **S3 Intelligent-Tiering** classifica automaticamente objetos em tiers de armazenamento (frequente/infrequente) para reduzir custos sem perda de acesso.  

## **2. Configuração Implementada**  
### **2.1. Regras de Transição**  
```yaml
Bucket: pague-menos-dados
LifecycleConfiguration:
  - ID: MoveToInfrequentAccess
    Status: Enabled
    Transition:
      DaysAfterCreation: 30
      StorageClass: INTELLIGENT_TIERING

Tiers Utilizados
Frequent Access: Dados acessados nos últimos 30 dias.

Infrequent Access: Dados não acessados por mais de 30 dias.

3. Caso de Uso na Pague Menos
3.1. Problema Identificado
60% dos dados no S3 Standard eram raramente acessados.

Custos elevados com armazenamento desnecessário.

3.2. Solução
Migração de 500 TB para Intelligent-Tiering.

Configuração de Lifecycle Policies para movimentação automática.

4. Vantagens
✔ Economia de 40% em custos de armazenamento.
✔ Zero taxas de recuperação para dados movidos entre tiers.
✔ Monitoramento via S3 Analytics.

5. Próximas Melhorias
Adicionar S3 Glacier para arquivamento de longo prazo.

Automatizar relatórios de acesso com AWS Athena.

Assinatura: Jonson Rodrigues Alves
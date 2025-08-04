* GFT Start 7 Boot Camp 2025

* Relatório de Implementação de Serviços AWS
* Data: 04/08/2025
* Empresa: Pague Menos
* Responsável: Jonson Rodrigues Alves

* INTRODUÇÃO
* Este relatório apresenta o processo de implementação de ferramentas AWS na empresa Pague Menos, realizado 
por Jonson Rodrigues Alves. O objetivo do projeto foi selecionar e implementar 3 serviços AWS com a finalidade de 
reduzir custos operacionais imediatos, melhorando a eficiência e a escalabilidade da infraestrutura de TI.
 
* DESCRIÇÃO
* O projeto foi dividido em 3 etapas, cada uma com objetivos específicos relacionados à implementação de ferramentas AWS. 
* Abaixo estão detalhadas as etapas:
 
* ETAPA 1: EC2 AUTO SCALING
* Foco da Ferramenta
* Escalabilidade automática de instâncias EC2 para otimizar custos e desempenho.
 
* Descrição de Caso de Uso
* A Pague Menos possuía servidores subutilizados em horários de baixa demanda e sobrecarregados em picos (como promoções).
 
* O EC2 Auto Scaling foi configurado para:
* Aumentar o número de instâncias automaticamente durante picos de tráfego.
* Reduzir instâncias quando a demanda diminuir, evitando custos desnecessários.
 
* Vantagens
* ✔ Redução de custos (paga apenas pelo uso real).
* ✔ Alta disponibilidade (evita downtime em picos de demanda).
* ✔ Otimização automática sem intervenção manual.
 
* ETAPA 2: S3 INTELLIGENT TIERING
* Foco da Ferramenta
* Armazenamento de dados com custo otimizado, movendo automaticamente arquivos entre tiers conforme frequência de acesso.
 
* Descrição de Caso de Uso
* A empresa armazenava grandes volumes de dados no S3 Standard, mesmo que alguns arquivos fossem raramente acessados.
 
* O S3 Intelligent-Tiering foi implementado para:
* Armazenar automaticamente dados em tiers diferentes (frequente/infrequente).
* Reduzir custos sem sacrificar acessibilidade.
 
* Vantagens
* ✔ Economia imediata (até 40% em armazenamento para dados pouco acessados).
* ✔ Gestão automática (sem overhead manual).
* ✔ Sem taxas de recuperação para dados movidos entre tiers.
 
* ETAPA 3: AMAZON RDS (AURORA SERVERLESS)
* Foco da Ferramenta
* Banco de dados gerenciado com escalonamento automático e ajuste de capacidade sob demanda.
 
* Descrição de Caso de Uso
* A Pague Menos utilizava bancos de dados provisionados manualmente, gerando custos fixos altos mesmo em períodos ociosos.
 
* O Amazon Aurora Serverless foi implantado para:
* Escalonar automaticamente recursos de banco de dados conforme a demanda.
* Reduzir custos em até 70% comparado a instâncias tradicionais.
 
* Vantagens
* ✔ Custo-efetivo (paga apenas pelo uso computacional real).
* ✔ Zero gerenciamento de servidores.
* ✔ Alta disponibilidade e desempenho automático.
 
````mermaid
classDiagram
    class EC2_AutoScaling {
        <<Serviço AWS>>
        -EscalonamentoAutomático: boolean
        -MinInstancias: int
        -MaxInstancias: int
        +OtimizarCustos()
        +AjustarCapacidade()
    }
    
    class S3_IntelligentTiering {
        <<Serviço AWS>>
        -TierFrequente: boolean
        -TierInfrequente: boolean
        +MoverDadosAutomaticamente()
        +ReduzirCustosArmazenamento()
    }
    
    class RDS_AuroraServerless {
        <<Serviço AWS>>
        -EscalaAutomatica: boolean
        -CustoPorUso: boolean
        +GerenciarBancoDeDados()
        +ReduzirCustosDB()
    }
    
    class PagueMenos {
        -Nome: String
        -Setor: String
        +ImplementarSolucoesAWS()
    }
    
    EC2_AutoScaling --> PagueMenos : "Reduz custos de infraestrutura"
    S3_IntelligentTiering --> PagueMenos : "Otimiza armazenamento"
    RDS_AuroraServerless --> PagueMenos : "Diminui custos de banco de dados"

````
* CONCLUSÃO
* A implementação desses 3 serviços AWS trouxe redução de custos imediata para a Pague Menos, além de melhorar a 
* eficiência operacional. As principais economias foram:

* EC2 Auto Scaling: Redução de ~30% em custos com infraestrutura.
* S3 Intelligent-Tiering: Economia de ~40% em armazenamento.
* Amazon RDS Serverless: Corte de ~70% em custos de banco de dados.
 
* Próximos passos: Monitorar métricas de desempenho e avaliar a expansão do uso de serviços AWS para outras 
* áreas da empresa.
 
* Assinatura: Jonson Rodrigues Alves
* Cargo: Analista de TI
* Empresa: Pague Menos
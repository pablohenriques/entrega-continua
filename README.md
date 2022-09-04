# Anotações. Curso Alura: Entrega Contínua - Qualidade e Confiabilidade
---

## Parte 01
---

- Clientes satisfeitos com a entrega de valor
- Deploys contínuas e automatizados
- Pipeline de deploy: -> design <--> build <--> teste <--> homologação <--> release/operações <-
- Colaboração é importante na equipe (feedback, melhoria e aprendizagem frequentes)
- Antipattern: gerenciamento manual de ambientes
    - ambientes tratados como código, versionados e criados de maneira automatizada
    - regras: escolher a versão do release; click no "deploy button"
- Antipattern: deploy manual
- Antipattern: deploy apenas no fim do ciclo
    - regras: deployment faz parte do desenvolvimento desde da primeira interação
- Entrega x Deploy
    - Na entrega contínua há necessidade de aprovação humana
    - No deploy contínuo não há necessidade de apravação, entrega é automatizada

## Parte 02
---

- Entrega contínua
    - Build automatizado
    - Testes automatizados
    - Gerenciamento de configuração

- Princípios
    - Automatize; Versione; Repita; Geranta qualidade; Defina "done"; Criar delivery team; Usar Melhoria Contínua

- Elementos
    - Cultura DevOps: feedback, colaboração, confiança
    - Melhoria e aprendizagem contínua

- Patterns
    - deployment pipeline
    - deploy patterns (blue/green, canary, feature toggle)

- Arquitetura
    - Novas propriedades: testability, deployability
    - SOLID, Services, 12 Factor App

## Parte 03
---

- Etapas (Confiança; Ambiente de Produção)
    - Build/Unit Test
    - Testes de aceitação automatizados
    - Homoloagação/UAT
    - Produção
    - Feedback

- Boas práticas
    - Pipeline é a única forma de deploy
    - manter o pipeline o mais rápido possível
    - build apenas uma vez
    - build independente do ambiente
    - ambientes iguais/semelhantes
    - ambientes efêmeros (temporários)
    - deploy para ambientes de maneira igual

## Parte 04
---

- Commit Stage
    - Tudo no repositório
    - Todo mundo acessa os artefatos
    - Todo o time é responsável
    - Menos de 10 min

- Testes de Aceitação Automatizados
    - São caros de escrever e manter
    - Configurar o ambiente
    - Deploy da aplicação
    - Rodar smoke tests
    - Rodas os testes

- Stage de Homologação
    - Testes manuais pelo cliente
    - Validar o software
    - Usa desde início (contínua)
    - Equipe deve participar (feedback)
    - * Teste de carga:
        - Testar a capacidade do software
        - Estabelecer metas claras e saber a baseline
        - Usar ferramentas de monitoração
        - Não precisam rodar a cada build, mas precisam ter um ciclo

## Parte 05
---

- Estratégias de releases
    - Deploy: Ambiente; Instalação do Software; Configuração do software
    - Release: Publicação (rollout); Deixar visível para o cliente
    - Release Pattern: Evitar que a aplicação fique offline durante o deploy (zero downtime); Rollback;
    - Blue/Green Deployment
        - Blue: versão atual
        - Green: versão verde 
    - Canary Releases
        - Versões em paralelo
        - Apenas alguns usuário usam
    - Feature Toggles (Feature Flags)
        - Configuração que permite versões em pararelo
    - The  Twelve-Factor App
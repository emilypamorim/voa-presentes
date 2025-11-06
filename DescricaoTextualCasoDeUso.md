# Descrição Textual dos Casos de Uso (Semana 2)

## 1. Caso de Uso: CU02 - Reservar Presente

| Campo | Detalhes |
| :--- | :--- |
| **Nome** | Reservar Presente |
| **Ator Principal** | Padrinho (Doador) |
| **Objetivo** | Permitir que um Padrinho selecione e reserve um desejo de presente de um idoso, garantindo a exclusividade da doação. |
| **Pré-Condição** | O Padrinho está na página de Desejos. O presente tem o `Status` "Disponível". |
| **Pós-Condição** | O presente tem seu `Status` alterado para "Reservado" e está associado a um registro de Padrinho. |
| **Fluxo Principal** | 1. O Padrinho escolhe um presente e clica em "Apadrinhar". 2. O sistema exibe um formulário para coleta de dados do Padrinho (Nome, WPP, Email). 3. O Padrinho confirma a reserva. 4. O sistema verifica a disponibilidade e registra o Padrinho, mudando o `Status` do Desejo para "Reservado". 5. O sistema exibe a confirmação e as orientações de entrega (contatos, endereço, prazo). |
| **Fluxos Alternativos**| **A1: Presente Indisponível (Conflito):** Se o presente for reservado por outro Padrinho no mesmo instante, o sistema nega a reserva, mantém o `Status` inalterado e exibe uma mensagem de erro, orientando o Padrinho a escolher outro item. |

---

## 2. Caso de Uso: CU04 - Monitorar Apadrinhamentos

| Campo | Detalhes |
| :--- | :--- |
| **Nome** | Monitorar Apadrinhamentos |
| **Ator Principal** | Administrador (ONG VOA) |
| **Objetivo** | Fornecer ao Administrador uma visão completa e atualizada do progresso da campanha e permitir a confirmação final da doação. |
| **Pré-Condição** | O Administrador está logado no sistema (CU05 - Autenticar no Sistema). |
| **Pós-Condição** | O Administrador possui informações atualizadas. O `Status` dos Desejos reflete a situação real (Reservado ou Entregue). |
| **Fluxo Principal** | 1. O Administrador acessa o painel de monitoramento. 2. O sistema exibe uma lista de todos os Desejos com `Status` e dados do Padrinho (se reservado). 3. O Administrador localiza um Desejo que foi fisicamente entregue à ONG. 4. O Administrador clica em "Confirmar Entrega". 5. O sistema altera o `Status` do Desejo para "Entregue" e registra a data da confirmação. |
| **Fluxos Alternativos**| **A1: Contato do Padrinho:** O Administrador pode clicar no nome de um Padrinho com `Status` "Reservado" para visualizar e copiar o contato, facilitando o follow-up logístico. |
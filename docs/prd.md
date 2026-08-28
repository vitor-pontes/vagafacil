# PRD - Product Requirements Document: VagaFácil

## 1. Visão Geral do Produto
O **VagaFácil** é uma aplicação web responsiva projetada para a gestão simplificada de veículos em estacionamentos rotativos. O sistema permite controlar a entrada de veículos, gerenciar condutores, monitorar vagas disponíveis e consultar condições externas via integração de APIs.

## 2. Público-Alvo
* Operadores de estacionamento e atendentes de guichê.
* Gerentes de pátio que necessitam de métricas rápidas sobre a ocupação do espaço.

## 3. Páginas da Aplicação
1. **Dashboard (Home):** Painel geral exibindo vagas ocupadas, resumo do dia e previsão do tempo local.
2. **Cadastro de Veículos/Condutores:** Formulário para registrar entrada de veículos com autopreenchimento de endereço.
3. **Gerenciamento do Pátio:** Tabela/Cards com a listagem dos veículos estacionados e opções de checkout.

## 4. User Stories e Critérios de Aceitação

* **US01:** Como operador, quero cadastrar a entrada de um veículo informando placa e dados do condutor para registrar a ocupação da vaga.
  * **Critérios de Aceitação:**
    * O sistema deve validar a placa no formato nacional (ABC-1234) ou Mercosul (ABC1D23).
    * Todos os campos obrigatórios (placa, modelo, condutor) devem ser preenchidos antes do salvamento.
    * Deve ser registrada a data e hora exata da entrada automaticamente.

* **US02:** Como operador, quero digitar o CEP do condutor e ter o endereço preenchido automaticamente para agilizar o atendimento.
  * **Critérios de Aceitação:**
    * Ao digitar 8 dígitos no campo CEP, o sistema deve consultar a API do ViaCEP.
    * Os campos Logradouro, Bairro, Cidade e UF devem ser preenchidos automaticamente.
    * Caso o CEP seja inválido, o sistema deve exibir uma mensagem de alerta visual para o usuário.

* **US03:** Como operador, quero visualizar os veículos atualmente estacionados em uma tabela responsiva para gerenciar o pátio.
  * **Critérios de Aceitação:**
    * A listagem deve exibir placa, modelo, hora de entrada e status de cada veículo.
    * Cada linha da tabela deve possuir um botão para registrar a saída (checkout).
    * O layout deve se adaptar sem quebras em telas mobile e desktop.

* **US04:** Como gerente, quero visualizar no dashboard a previsão do tempo atual para prever o fluxo de veículos.
  * **Critérios de Aceitação:**
    * O dashboard deve consumir uma API pública de clima e exibir a temperatura atual da cidade.
    * Em caso de falha no carregamento da API, deve ser exibida uma mensagem amigável sem quebrar o layout.
    * 
## 5. Regras de Negócio
* A placa do veículo deve seguir obrigatoriamente o padrão nacional antigo (ABC-1234) ou Mercosul (ABC1D23).
* É obrigatório informar o CPF do condutor (com validação de formato).
* O sistema não deve permitir o registro de saída (checkout) sem a confirmação prévia da ação.

# Architecture Document: VagaFácil

## 1. Visão Geral da Arquitetura
O **VagaFácil** é uma aplicação web Front-End construída em arquitetura modular baseada em HTML5, CSS3/Sass e JavaScript Vanilla (ES6+), consumindo serviços REST assíncronos.

## 2. Tecnologias Utilizadas
* **HTML5:** Estruturação semântica das telas.
* **CSS3 / Sass:** Customização de estilos, variáveis e tipografia fluida.
* **Framework CSS:** Bootstrap 5 (incorporado via CDN).
* **JavaScript (ES6+):** Lógica da aplicação, manipulação do DOM e requisições assíncronas.
* **Bibliotecas JS:** jQuery e jQuery Mask Plugin (para aplicação de máscaras em inputs).

## 3. Integração com APIs
1. **ViaCEP API (Pública):**
   * **URL Base:** https://viacep.com.br/ws/{cep}/json/
   * **Objetivo:** Autopreenchimento de logradouro, bairro, cidade e estado no cadastro a partir do CEP informado.
2. **OpenWeatherMap API / HGFast Weather (Pública):**
   * **Objetivo:** Exibição da temperatura e clima atual no Dashboard.
3. **JSON Server (API Fake):**
   * **Objetivo:** Persistência assíncrona (CRUD) das entidades veiculos e clientes.

## 4. Entidades de Dados (JSON Server)
* **veiculos**: { id, placa, modelo, cor, horaEntrada, clienteId, status }
* **clientes**: { id, nome, cpf, telefone, cep, logradouro, numero }

## 4.1. Diagrama Entidade-Relacionamento (ER)

```mermaid
erDiagram
    CLIENTE ||--o{ VEICULO : possui
    CLIENTE {
        int id PK
        string nome
        string cpf
        string telefone
        string cep
        string logradouro
        string numero
    }
    VEICULO {
        int id PK
        string placa
        string modelo
        string cor
        string horaEntrada
        string status
        int clienteId FK
    }


  5. Design Tokens
Cores Principais:

Primary (Azul Principal): #0d6efd

Secondary (Cinza Neutro): #6c757d

Success (Status Livre/Ativo): #198754

Danger (Status Ocupado/Remoção): #dc3545

Background Light: #f8f9fa

Tipografia: System Font / Roboto (Sans-Serif com rem para dimensionamento responsivo).

6. Mapeamento de Componentes (Framework CSS)
Componentes do protótipo que serão substituídos por componentes nativos do Bootstrap 5:

Navbar: Navegação responsiva com menu hambúrguer para telas mobile.

Cards: Exibição resumida de estatísticas do pátio e informações de veículos.

Modal: Caixa de diálogo para confirmação de checkout de veículos.

# 🚗 VagaFácil - Sistema de Gestão de Estacionamento

## 👤 Autor
* **Nome:** Vitor Pontes

## 📝 Descrição do Projeto
O **VagaFácil** é uma aplicação web responsiva para gerenciamento de veículos em estacionamentos rotativos. O sistema permite controle de entrada e saída do pátio, cadastro de condutores com busca automática de endereço via CEP e exibição de informações climáticas em tempo real.

## 🎨 Design System e Prototipação
* **Prototipação no Stitch / Figma:** 
* **Design System & Arquitetura:** Documentado em [`docs/architecture.md`](docs/architecture.md)

## 🛠️ Tecnologias e Dependências
* **Framework CSS:** Bootstrap 5
* **Bibliotecas JavaScript:** jQuery, jQuery Mask Plugin
* **APIs:** 
  * API Pública: ViaCEP (Busca de Endereço) / OpenWeather (Clima)
  * API Fake: JSON Server (Persistência de Dados)

## 🌐 Site em Produção
* **Link GitHub Pages:** 

---

## 📖 Checklist de Funcionalidades (IDs)

### RA1 - Utilizar Frameworks CSS para estilização de elementos HTML e criação de layouts responsivos.
- [ ] **ID 01** - Prototipa interfaces adaptáveis (mobile/desktop) usando Figma/Stitch.
- [ ] **ID 02** - Implementa layout responsivo com Framework CSS (Bootstrap) usando Flexbox/Grid do próprio framework.
- [ ] **ID 03** - Implementa layout responsivo com CSS puro, usando Flexbox ou Grid Layout.
- [ ] **ID 04** - Utiliza componentes prontos de um Framework CSS (ex.: card, button, modal).
- [ ] **ID 05** - Cria layout fluido usando unidades relativas (vw, vh, %, em, rem).
- [ ] **ID 06** - Aplica um Design System consistente (cores, tipografia, padrões) em toda a aplicação.
- [ ] **ID 07** - Utiliza Sass (SCSS) aplicando variáveis, mixins e funções.
- [ ] **ID 08** - Aplica tipografia responsiva (mobile first ou `clamp()`).
- [ ] **ID 09** - Aplica técnicas de responsividade de imagens usando CSS.
- [ ] **ID 10** - Otimiza imagens usando formatos modernos (WebP) e carregamento adaptativo.

### RA2 - Realizar tratamento de formulários e aplicar validações customizadas no lado cliente.
- [ ] **ID 11** - Implementa validação HTML nativa com mensagens no lado cliente.
- [ ] **ID 12** - Aplica expressões regulares (REGEX) para validações customizadas (placa, CPF, etc.).
- [ ] **ID 13** - Utiliza elementos de seleção em formulários (checkbox, radio, select).
- [ ] **ID 14** - Implementa leitura e escrita no Web Storage (localStorage/sessionStorage).

### RA3 - Aplicar ferramentas para otimização do processo de desenvolvimento web.
- [ ] **ID 15** - Configura ambiente com Node.js e NPM para gerenciamento de pacotes.
- [ ] **ID 16** - Utiliza boas práticas de versionamento no Git/GitHub (commits, `.gitignore`).
- [x] **ID 17** - Mantém um README.md padronizado com checklist preenchido.
- [ ] **ID 18** - Organiza arquivos do projeto de forma modular.
- [ ] **ID 19** - Configura linters e formatadores (ESLint, Prettier).

### RA4 - Aplicar bibliotecas de funções e componentes em JavaScript para aprimorar a interatividade.
- [ ] **ID 20** - Utiliza jQuery para manipulação do DOM e interatividade.
- [ ] **ID 21** - Integra e configura um plugin jQuery relevante (jQuery Mask Plugin).

### RA5 - Efetuar requisições assíncronas para uma API fake e APIs públicas.
- [ ] **ID 22** - Realiza requisições assíncronas para API fake (JSON Server) para persistir dados.
- [ ] **ID 23** - Realiza requisições assíncronas para API fake para exibir dados na página.
- [ ] **ID 24** - Realiza requisições assíncronas para APIs públicas reais (ViaCEP), tratando erros.

---

## 🚀 Instruções de Execução
*(Serão preenchidas quando o servidor local / JSON Server for configurado)*

# 🏋️‍♂️ GYMPRO - Sistema de Gestão de Academias

> Projeto desenvolvido por **Leonardo Mendes** e **Luis Gustavo**

![Status do Projeto](https://img.shields.io/badge/Status-Conclu%C3%ADdo-success?style=for-the-badge)
![Tecnologia](https://img.shields.io/badge/Tecnologia-HTML%20%7C%20JS%20%7C%20Tailwind-blue?style=for-the-badge)
![Deploy](https://img.shields.io/badge/Deploy-Vercel-black?style=for-the-badge&logo=vercel)

Bem-vindo ao repositório do **GymPro**, um Sistema de Gestão de Academias de Alta Performance projetado para erradicar a desorganização manual e transformar a gestão operacional em vantagem competitiva.

🔗 **[Acessar a Aplicação Online](https://projeto-eng-software.vercel.app/)**
📄 **[Documentação Completa do Projeto](https://docs.google.com/document/d/1uufTo7toRpvh_lM74xhkrH4LEi9ucQ52AkW-kmDFUGk/edit?usp=sharing)**
🎨 **[Visualizar Protótipo no Figma](https://www.figma.com/proto/v2yRgKh6XKDGlYAjGkdAGP/Sistema-GYMPRO-%F0%9F%92%AA%F0%9F%8F%BC?node-id=38-205&p=f&t=p3tIqphdbsjgQVty-1&scaling=contain&content-scaling=fixed&page-id=0%3A1)**
📊 **[Apresentação do Projeto (Apresentação Técnica)](https://docs.google.com/presentation/d/1Z2L1ycrcM6NeUvRZzqK0MxSilha_Il-uBQknfHjxwgY/edit?usp=sharing)**

---

## 🎯 Sobre o Projeto

A gestão manual ineficiente (uso de planilhas isoladas ou papel) causa perda de dados de evolução, inadimplência e desorganização. Isso contribui para que **45% das academias** percam seus alunos logo no primeiro trimestre. 

O **GymPro** surge como a solução para interromper esse "efeito cascata", oferecendo uma interface administrativa responsiva, intuitiva e moderna, centralizando a gestão de alunos, instrutores e planos de forma eficaz.

---

## 📋 Levantamento de Requisitos

Abaixo estão detalhados os requisitos mapeados para o funcionamento da aplicação, divididos de forma estruturada.

### Requisitos Funcionais (RF)

| Identificador | Descrição do Requisito |
| :--- | :--- |
| **RF01** | O sistema deve possuir um *Dashboard* exibindo métricas atualizadas do total de alunos, professores e planos cadastrados. |
| **RF02** | O sistema deve permitir o cadastro, listagem e remoção de Alunos informando Nome, Idade, Peso, Altura e Plano associado. |
| **RF03** | O sistema deve permitir o cadastro, listagem e remoção de Professores informando Nome, Idade e CREF. |
| **RF04** | O sistema deve permitir o cadastro, listagem e exclusão de Planos de treino detalhando Nome, Descrição, Frequência e Preço. |

### Requisitos Não Funcionais (RNF)

| Identificador | Descrição do Requisito |
| :--- | :--- |
| **RNF01** | A interface de usuário (UI) deve ser desenvolvida utilizando a abordagem *Mobile First* garantindo responsividade total. |
| **RNF02** | O sistema deve ser construído utilizando HTML5, JavaScript (Vanilla) e estilizado com o framework Tailwind CSS. |

### Regras de Negócio (RN)

| Identificador | Regra Aplicada |
| :--- | :--- |
| **RN01** | Todo aluno cadastrado no sistema deve possuir um vínculo obrigatório com pelo menos um plano ativo (Relação 1,1). |
| **RN02** | O cadastro de professores exige a validação e inserção de um registro profissional válido (CREF). |

---

## 🛠️ Tecnologias Utilizadas

| Componente | Tecnologia | Propósito |
| :--- | :--- | :--- |
| **Estrutura** | `HTML5` | Marcação semântica e estruturação de dados. |
| **Estilização** | `Tailwind CSS` | Framework utilitário para design responsivo e interface moderna (Modo Dark). |
| **Lógica e Estado** | `JavaScript (Vanilla)` | Gerenciamento de estado visual da interface (DOM) e simulação de rotas (SPA). |
| **Ícones** | `Lucide Icons` | Biblioteca de ícones vetoriais leves e consistentes. |
| **Design** | `Figma` | Prototipação de alta fidelidade e UI/UX design. |

---

## 🗄️ Modelagem de Dados

O sistema foi arquitetado com base em um modelo relacional sólido para organizar as informações da academia.

### Dicionário de Dados

| Tabela | Campos Principais | Tipo de Dado |
| :--- | :--- | :--- |
| **USUARIO** | `id`, `email`, `senha` | INT, VARCHAR, VARCHAR |
| **PLANO** | `id`, `nome`, `descricao`, `frequencia`, `preco` | INT, VARCHAR, VARCHAR, VARCHAR, DECIMAL |
| **ALUNO** | `id`, `nome`, `idade`, `peso`, `altura`, `plano_id` (FK) | INT, VARCHAR, INT, DECIMAL, DECIMAL, INT |
| **PROFESSOR** | `id`, `nome`, `idade`, `cref` | INT, VARCHAR, INT, VARCHAR |

---

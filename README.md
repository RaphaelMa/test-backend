## Desafio para o Candidato - Desenvolvedor Backend Sênior em NestJS

# Objetivo
Desenvolver um sistema backend utilizando NestJS para gerenciar acessos aos módulos CompanyController e ProductsController. Cada usuário tem acesso a determinados módulos, representados pelos controllers. O acesso do usuário será validado por meio de um interceptor que verificará se o usuário tem permissão para acessar o módulo da requisição.

# Requisitos
Implementar dois controllers: CompanyController e ProductsController.
Criar um interceptor para validar o acesso do usuário aos módulos.
Utilizar um mock de dados para representar os usuários e seus respectivos módulos. Cada usuário possui um id, email e modules, onde modules é uma lista de objetos contendo o name do módulo.
O interceptor deve extrair o email do usuário da requisição e verificar se o usuário tem acesso ao módulo correspondente ao controller. Se não tiver acesso, a requisição deve ser bloqueada, e uma exceção ForbiddenException deve ser lançada.

## MOCK
export const MockData = [
  {
    id: "3a5c1aa7-81d1-4b27-8f55-6f3f8c48b5e2",
    email: "company@teste.com.br",
    modules: [
      {
        name: "company",
      },
    ],
  },
  {
    id: "c6e70325-c0a9-4a2a-a167-5579d07e9ea5",
    email: "produto@teste.com.br",
    modules: [
      {
        name: "products",
      },
    ],
  },
];

# Observações
O candidato deve implementar a lógica do interceptor para validar o acesso aos controllers com base nos módulos do usuário.
A estrutura do NestJS, como módulos, serviços, etc., deve ser considerada na implementação.
A lógica do interceptor deve ser extensível para a inclusão de novos módulos e controllers no futuro.


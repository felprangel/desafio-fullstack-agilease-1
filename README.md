# Desafio Full-Stack - Sistema de Registros de Leitura

Primeiramente, obrigado pelo seu interesse em participar deste desafio técnico!
Abaixo você encontrará todas as informações necessárias para iniciar o desenvolvimento.

## Avisos antes de começar

- Leia com atenção este documento todo e tente seguir ao **máximo** as instruções;
- Crie um repositório no seu GitHub **público** para o projeto;
- Faça commits regulares e descritivos no seu repositório;
- Você poderá consultar o Google, Stack Overflow ou qualquer documentação oficial;
- Fique à vontade para tirar dúvidas durante o desenvolvimento;

### Sobre o ambiente da aplicação:

**Frontend:**
- Recomendamos fortemente o uso de **React com Next.js**, mas você pode escolher qualquer framework/biblioteca que se sinta **confortável** em trabalhar;
- Caso opte por outra tecnologia, esteja preparado para justificar sua escolha durante a apresentação;

**Backend:**
- Recomendamos fortemente o uso de **JavaScript/TypeScript com NestJS**, mas você pode escolher qualquer linguagem/framework que domine;
- Evite usar métodos mágicos ou ORMs muito abstratos. Queremos ver **seu** código e sua forma de resolver problemas;

> Valorizamos uma boa estrutura de containers e orquestração criada por você.

## Processo de avaliação

Após o envio do seu repositório, nossa equipe técnica fará uma análise completa do seu código, incluindo:

- **Code review detalhado**: Avaliaremos a qualidade do código, estrutura do projeto, padrões utilizados e boas práticas aplicadas;
- **Execução local**: Rodaremos sua aplicação localmente seguindo as instruções do README para testar todas as funcionalidades implementadas;
- **Análise arquitetural**: Verificaremos as decisões técnicas, modelagem de dados e estruturação geral da solução;

Certifique-se de que sua aplicação rode corretamente seguindo apenas as instruções do seu README, pois será assim que testaremos o projeto.

## Objetivo: Sistema de Registros de Leitura

O Sistema de Registros de Leitura é uma aplicação full-stack onde usuários podem cadastrar e gerenciar seus livros lidos, com informações detalhadas sobre cada leitura. O sistema deve permitir autenticação de usuários e operações CRUD completas para os registros de leitura.

### Requisitos Funcionais

#### Autenticação de Usuários
- Sistema de cadastro de usuários com `nome`, `email` e `senha`;
- Sistema de login com `email` e `senha`;
- Emails devem ser únicos no sistema;
- Senhas devem ser criptografadas antes de serem armazenadas;
- Sistema de logout;
- Middleware de autenticação para proteger rotas privadas;

#### CRUD de Registros de Leitura
Cada registro de leitura deve conter:
- `título` do livro (obrigatório);
- `autor` do livro (obrigatório);
- `gênero` do livro;
- `data de início` da leitura;
- `data de conclusão` da leitura;
- `avaliação` (nota de 1 a 5 estrelas);
- `resenha/comentários` pessoais;
- `status` da leitura (Lendo, Concluído, Pausado, Abandonado);

**Operações necessárias:**
- **CREATE**: Adicionar novo registro de leitura;
- **READ**: Listar todos os registros do usuário logado e visualizar detalhes de um registro específico;
- **UPDATE**: Editar informações de um registro existente;
- **DELETE**: Remover um registro de leitura;

#### Funcionalidades Adicionais
- Filtros por status da leitura;
- Busca por título ou autor;
- Ordenação por data de conclusão, avaliação ou título;

### Requisitos Técnicos

#### Backend
- API RESTful bem estruturada;
- Validação de dados de entrada;
- Tratamento adequado de erros;
- Middleware de autenticação JWT;
- Relacionamento correto entre usuários e registros de leitura;
- Docker Compose para orquestração do banco de dados e aplicação;
- Documentação da API (Swagger/OpenAPI é um plus);

#### Frontend
- Interface responsiva e intuitiva;
- Formulários com validação client-side;
- Gerenciamento de estado da aplicação;
- Tratamento de loading states e erros;
- Navegação protegida (usuários não autenticados não podem acessar rotas privadas);
- Design limpo e profissional;

#### Banco de Dados
- Modelagem adequada das entidades (User, ReadingLog);
- Relacionamentos corretos entre tabelas;
- Índices apropriados para consultas;
- Você pode usar o banco que mais tiver familiaridade;

# Avaliação

Apresente sua solução justificando as escolhas tecnológicas e arquiteturais.
Foque em cumprir os requisitos principais, mas não se preocupe se não conseguir implementar todas as funcionalidades adicionais.

## O que será avaliado e valorizamos :heart:

### Habilidades Fundamentais:
- Conhecimento de APIs RESTful;
- Uso adequado do Git com commits descritivos;
- Capacidade de análise e solução de problemas;
- Código limpo, organizado e legível;
- Estruturação adequada de projetos frontend e backend;

### Conhecimentos Intermediários:
- Implementação correta de autenticação e autorização;
- Validação de dados tanto no frontend quanto no backend;
- Tratamento adequado de erros e edge cases;
- Gerenciamento de estado no frontend;
- Relacionamentos e modelagem de banco de dados;
- Conhecimentos sobre containerização (Docker);
- Documentação clara do projeto;
- Testes unitários e/ou de integração;

### Aptidões Avançadas:
- Aplicação de design patterns adequados;
- Arquitetura escalável e manutenível;
- Otimizações de performance;
- Implementação de cache quando apropriado;
- Monitoramento e logging;
- Segurança (sanitização, rate limiting, etc.);
- Deployment e configuração de produção;

### Boas Práticas

**Backend (se usar NestJS/Node.js):**
- Seguir convenções do framework escolhido;
- Usar TypeScript quando possível;
- Separação clara de responsabilidades (Controllers, Services, Repositories);

**Frontend (se usar React/Next.js):**
- Componentes reutilizáveis e bem estruturados;
- Hooks customizados quando apropriado;
- Gerenciamento adequado do estado global;

## O que NÃO será avaliado :warning:

- Design gráfico elaborado (foque na funcionalidade e usabilidade);
- Deploy em produção (ambiente local é suficiente);
- Funcionalidades não especificadas nos requisitos;

## O que será um Diferencial

- Cobertura de testes abrangente;
- Documentação técnica detalhada;
- Interface responsiva e acessível;
- Implementação de funcionalidades extras bem pensadas;
- Considerações de segurança;
- Arquitetura que demonstre pensamento escalável;

## Docker Compose

Seu projeto deve incluir um arquivo `docker-compose.yml` que permita executar todo o ambiente com um único comando:

```bash
docker-compose up -d
```

Isso deve inicializar:
- Banco de dados com as configurações necessárias;
- Backend da aplicação;
- (Opcional) Frontend da aplicação;

## Como executar

Inclua no README do seu projeto instruções claras de como:
1. Clonar e configurar o projeto;
2. Instalar dependências;
3. Executar com Docker Compose;
4. Executar localmente para desenvolvimento;
5. Executar testes;

Boa sorte com o desenvolvimento! 🚀

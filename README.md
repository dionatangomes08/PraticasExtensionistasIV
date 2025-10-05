# 🏠 PrestaServ

**Uma plataforma completa para conectar prestadores de serviços e clientes**

PrestaServ é uma solução full-stack que facilita a conexão entre prestadores de serviços e clientes, oferecendo uma experiência intuitiva tanto para mobile quanto para web.

## 📱 Visão Geral

O projeto consiste em duas aplicações principais:

- **🖥️ API Backend** (`prestaserv-api`) - API RESTful robusta desenvolvida com NestJS
- **📱 App Mobile** (`prestaserv-front`) - Aplicativo móvel desenvolvido com React Native e Expo

## 🚀 Tecnologias Utilizadas

### Backend (prestaserv-api)
- **NestJS** - Framework Node.js modular e escalável
- **TypeScript** - Tipagem estática para JavaScript
- **TypeORM** - ORM para TypeScript e JavaScript
- **PostgreSQL** - Banco de dados relacional
- **JWT** - Autenticação e autorização
- **Passport** - Middleware de autenticação
- **bcrypt** - Hash de senhas
- **Class Validator** - Validação de dados

### Frontend (prestaserv-front)
- **React Native** - Framework para desenvolvimento mobile
- **Expo** - Plataforma de desenvolvimento React Native
- **TypeScript** - Tipagem estática
- **Expo Router** - Navegação moderna para Expo
- **React Navigation** - Navegação entre telas
- **AsyncStorage** - Armazenamento local
- **React Native Calendars** - Componente de calendário

## 🏗️ Arquitetura do Sistema

### API Backend
```
prestaserv-api/
├── src/
│   ├── app.module.ts          # Módulo principal
│   ├── main.ts               # Ponto de entrada
│   ├── usuarios/             # Módulo de usuários
│   ├── servicos/            # Módulo de serviços
│   ├── contratos/           # Módulo de contratos
│   └── usuarios-servicos/   # Relação usuários-serviços
└── test/                    # Testes automatizados
```

### App Mobile
```
prestaserv-front/
├── app/
│   ├── (auth)/              # Telas de autenticação
│   ├── (tabs)/             # Navegação por abas
│   ├── cliente/            # Área do cliente
│   └── prestador/          # Área do prestador
├── components/             # Componentes reutilizáveis
└── assets/                # Recursos estáticos
```

## ⚡ Funcionalidades

### 👥 Sistema de Usuários
- ✅ Cadastro e autenticação de usuários
- ✅ Perfis diferenciados (Cliente/Prestador)
- ✅ Gerenciamento de perfil
- ✅ Sistema de autenticação JWT

### 🔧 Gestão de Serviços
- ✅ Cadastro de serviços pelos prestadores
- ✅ Listagem e busca de serviços
- ✅ Categorização de serviços
- ✅ Avaliações e comentários

### 📋 Sistema de Contratos
- ✅ Solicitação de serviços
- ✅ Gerenciamento de contratos
- ✅ Acompanhamento de status
- ✅ Histórico de serviços

## 🛠️ Instalação e Configuração

### Pré-requisitos
- Node.js (v18 ou superior)
- PostgreSQL
- Expo CLI
- Git

### 🗄️ Backend (API)

1. **Clone o repositório**
```bash
git clone [url-do-repositorio]
cd prestaserv-api
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure o banco de dados**
- Crie um banco PostgreSQL chamado `prestaserv_db`
- Configure as credenciais em `src/app.module.ts`

4. **Execute a aplicação**
```bash
# Desenvolvimento
npm run start:dev

# Produção
npm run build
npm run start:prod
```

A API estará disponível em `http://localhost:3000`

### 📱 Frontend (Mobile)

1. **Navegue para o diretório**
```bash
cd prestaserv-front
```

2. **Instale as dependências**
```bash
npm install
```

3. **Execute a aplicação**
```bash
# Desenvolvimento
npm start

# Para Android
npm run android

# Para iOS
npm run ios

# Para Web
npm run web
```

## 📊 Endpoints da API

### Autenticação
- `POST /auth/login` - Login de usuário
- `POST /auth/register` - Registro de usuário

### Usuários
- `GET /usuarios` - Listar usuários
- `GET /usuarios/:id` - Buscar usuário por ID
- `PUT /usuarios/:id` - Atualizar usuário
- `DELETE /usuarios/:id` - Remover usuário

### Serviços
- `GET /servicos` - Listar serviços
- `POST /servicos` - Criar serviço
- `GET /servicos/:id` - Buscar serviço por ID
- `PUT /servicos/:id` - Atualizar serviço
- `DELETE /servicos/:id` - Remover serviço

### Contratos
- `GET /contratos` - Listar contratos
- `POST /contratos` - Criar contrato
- `GET /contratos/:id` - Buscar contrato por ID
- `PUT /contratos/:id` - Atualizar contrato

## 🧪 Testes

### Backend
```bash
# Testes unitários
npm run test

# Testes com watch
npm run test:watch

# Testes de cobertura
npm run test:cov

# Testes E2E
npm run test:e2e
```

### Frontend
```bash
# Executar linter
npm run lint
```

## 📦 Scripts Disponíveis

### Backend
- `npm run start:dev` - Executa em modo desenvolvimento
- `npm run build` - Compila o projeto
- `npm run lint` - Executa ESLint
- `npm run format` - Formata código com Prettier

### Frontend
- `npm start` - Inicia o servidor Expo
- `npm run android` - Executa no Android
- `npm run ios` - Executa no iOS
- `npm run web` - Executa na web

## 🔒 Segurança

- ✅ Autenticação JWT
- ✅ Hash de senhas com bcrypt
- ✅ Validação de dados de entrada
- ✅ CORS configurado
- ✅ Sanitização de inputs

## 📈 Roadmap

- [ ] Sistema de notificações push
- [ ] Chat em tempo real
- [ ] Sistema de pagamentos
- [ ] Avaliações e comentários avançados
- [ ] Geolocalização de serviços
- [ ] Dashboard administrativo
- [ ] API de terceiros (Google Maps, etc.)

## 🤝 Contribuindo

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença [UNLICENSED]. Veja o arquivo `LICENSE` para mais detalhes.

## 👨‍💻 Autores

**Jordan Neves**
- GitHub: [@jordanneves](https://github.com/jordanneves)
**Dionatan Gomes**
- GitHub: [@dionatangomes08](https://github.com/dionatangomes08)
**Fabricio Ludwig Perozzo**
**Marcelo Margreiter**

## 📞 Suporte

Se você encontrar algum problema ou tiver dúvidas:

1. Verifique se já existe uma [issue](https://github.com/jordanneves/prestaserv-api/issues) relacionada
2. Crie uma nova issue com detalhes do problema
3. Entre em contato através do GitHub

---

⭐ **Gostou do projeto? Deixe uma estrela!** ⭐

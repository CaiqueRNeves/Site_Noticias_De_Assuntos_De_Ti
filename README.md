# Site De Notícias de Ti

Um site completo com sistema de autenticação, painel administrativo, publicação de matérias e galeria de memes.

## Características

- **Design Responsivo**: Interface adaptável para desktop, tablet e dispositivos móveis
- **Menu Lateral Retrátil**: Menu que pode ser expandido ou recolhido para melhor experiência do usuário
- **Esquema de Cores Personalizável**: Tons de azul bebê e branco em estilo pastel
- **Sistema de Autenticação Seguro**: Registro de usuários, login/logout e proteção de rotas
- **Painel Administrativo Completo**: Gerenciamento de conteúdo, usuários e configurações do site
- **Editor de Texto Avançado**: Editor rico para criação de matérias com formatação completa
- **Galeria de Memes**: Sistema para compartilhamento e download de imagens e vídeos
- **Banco de Dados MySQL**: Armazenamento seguro de dados de usuários, matérias e mídias

## Tecnologias Utilizadas

- **Frontend**: Next.js, React, Tailwind CSS
- **Backend**: Next.js API Routes
- **Banco de Dados**: MySQL
- **Autenticação**: NextAuth.js, bcrypt
- **Editor de Texto**: React Quill
- **Estilização**: Tailwind CSS

## Estrutura do Projeto

```
site-multimidia/
├── migrations/              # Scripts SQL para criação do banco de dados
├── public/                  # Arquivos estáticos
├── src/
│   ├── app/                 # Páginas da aplicação (Next.js App Router)
│   │   ├── admin/           # Páginas do painel administrativo
│   │   ├── api/             # Rotas de API
│   │   ├── cadastro/        # Página de cadastro de usuários
│   │   ├── galeria/         # Páginas da galeria de memes
│   │   ├── login/           # Página de login
│   │   ├── materias/        # Páginas de matérias
│   │   └── ...
│   ├── components/          # Componentes reutilizáveis
│   │   ├── admin/           # Componentes do painel administrativo
│   │   └── layout/          # Componentes de layout
│   └── lib/                 # Utilitários e funções
│       ├── auth/            # Funções de autenticação
│       └── db/              # Funções de acesso ao banco de dados
└── tests/                   # Testes de segurança e funcionalidades
```

## Requisitos

- Node.js 18.0 ou superior
- MySQL 8.0 ou superior

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/site-multimidia.git
   cd site-multimidia
   ```

2. Instale as dependências:
   ```bash
   npm install
   # ou
   pnpm install
   ```

3. Configure as variáveis de ambiente:
   Crie um arquivo `.env.local` na raiz do projeto com as seguintes variáveis:
   ```
   MYSQL_HOST=localhost
   MYSQL_PORT=3306
   MYSQL_DATABASE=site_multimidia
   MYSQL_USER=seu_usuario
   MYSQL_PASSWORD=sua_senha
   NEXTAUTH_SECRET=sua_chave_secreta
   NEXTAUTH_URL=http://localhost:3000
   ```

4. Crie o banco de dados:
   ```bash
   mysql -u root -p
   ```
   ```sql
   CREATE DATABASE site_multimidia;
   ```

5. Execute o script de migração:
   ```bash
   mysql -u root -p site_multimidia < migrations/0001_initial.sql
   ```

6. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   # ou
   pnpm dev
   ```

7. Acesse o site em [http://localhost:3000](http://localhost:3000)

## Usuário Administrador Padrão

- **Email**: admin@exemplo.com
- **Senha**: admin123

## Funcionalidades

### Usuários Comuns
- Visualizar matérias publicadas
- Navegar pela galeria de memes
- Fazer download de imagens e vídeos (requer login)
- Gerenciar perfil pessoal

### Administradores
- Todas as funcionalidades de usuários comuns
- Acesso ao painel administrativo
- Gerenciamento de matérias (criar, editar, excluir)
- Gerenciamento da galeria de memes (adicionar, editar, excluir)
- Configurações do site (cores, opções de exibição)

## Personalização

### Cores
As cores do site podem ser personalizadas no arquivo `src/app/globals.css`, modificando as variáveis CSS na seção `:root`.

### Layout
O layout do site pode ser ajustado modificando os componentes em `src/components/layout/`.



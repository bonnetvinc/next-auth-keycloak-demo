# Gate Keeper - Next.js + NextAuth + Keycloak

Authentication demonstration project with [Next.js](https://nextjs.org/), [NextAuth.js](https://next-auth.js.org/) and [Keycloak](https://www.keycloak.org/).

Stack: [T3 Stack](https://create.t3.gg/) - Next.js, tRPC, Prisma, TailwindCSS

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18.0 or higher
- **pnpm** (package manager) - [Installation](https://pnpm.io/installation)
- **Docker** and **Docker Compose** (for PostgreSQL and Keycloak)

### Installation

1. **Clone the project**

```bash
git clone <repository-url>
cd next-auth-keycloak-demo
```

2. **Install dependencies**

```bash
pnpm install
```

3. **Configure environment variables**
   Create a `.env` file at the root of the project:

```bash
cp .env.example .env
```

Then edit `.env` with your settings (database, Keycloak, etc.)

### Running the project

#### With Docker Compose

1. **Start services (PostgreSQL + Keycloak)**

```bash
make start-tools
```

2. **Initialize the database**

```bash
pnpm run db:push
```

3. **Start the application in development mode**

```bash
pnpm run dev
```

The application will be available at: **http://localhost:3000**


## 📝 Available Commands

| Command                | Description                                  |
| ---------------------- | -------------------------------------------- |
| `pnpm run dev`         | Start the development server with Turbo      |
| `pnpm run build`       | Build the application for production         |
| `pnpm run start`       | Launch the production build                  |
| `pnpm run preview`     | Build and preview the application            |
| `pnpm run db:push`     | Sync Prisma schema with database             |
| `pnpm run db:migrate`  | Apply Prisma migrations                      |
| `pnpm run db:generate` | Generate Prisma migrations                   |
| `pnpm run db:studio`   | Open Prisma Studio to view data              |
| `pnpm run check`       | Check code with Biome                        |
| `pnpm run check:write` | Format code with Biome                       |
| `pnpm run typecheck`   | Check TypeScript types                       |
| `make start-tools`     | Start Docker services (PostgreSQL, Keycloak) |

## 🛠️ Architecture

- **Frontend**: Next.js 15 with React 19
- **Backend**: Next.js API Routes + tRPC
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js v5 + Keycloak
- **Styling**: TailwindCSS
- **Linting**: Biome

## 📚 Resources

- [T3 Stack Documentation](https://create.t3.gg/)
- [Next.js Documentation](https://nextjs.org/docs)
- [NextAuth.js Documentation](https://next-auth.js.org/)
- [Prisma Documentation](https://www.prisma.io/docs/)
- [Keycloak Documentation](https://www.keycloak.org/documentation)

## 📄 License

MIT

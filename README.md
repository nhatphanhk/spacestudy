# Study Space 📚

A modern, collaborative study platform built with Next.js that helps students organize their learning materials, track progress, and study effectively.

## ✨ Features

- **Study Sessions**: Create and manage focused study sessions with timers
- **Note Taking**: Rich text editor for creating and organizing study notes
- **Flashcards**: Interactive flashcard system for memorization
- **Progress Tracking**: Visual analytics of study time and performance
- **Study Groups**: Collaborate with other students in virtual study rooms
- **Task Management**: To-do lists and assignment tracking
- **Pomodoro Timer**: Built-in productivity timer with break reminders
- **Dark/Light Mode**: Customizable theme preferences

## 🛠️ Tech Stack

- **Framework**: [Next.js 14](https://nextjs.org/) with App Router
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)
- **Database**: PostgreSQL with [Prisma ORM](https://www.prisma.io/)
- **Authentication**: [NextAuth.js](https://next-auth.js.org/)
- **Icons**: [Lucide Icons](https://lucide.dev/)
- **Deployment**: [Vercel](https://vercel.com/)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Node.js 18.0 or later
- npm or yarn or pnpm
- PostgreSQL database
- Git

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/study-space.git
cd study-space
```

### 2. Install dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3. Set up environment variables

Create a `.env.local` file in the root directory:

```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/study_space"

# NextAuth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key-here"

# OAuth Providers (optional)
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"

# Other services (optional)
UPLOADTHING_SECRET="your-uploadthing-secret"
UPLOADTHING_APP_ID="your-uploadthing-app-id"
```

### 4. Set up the database

```bash
# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma db push

# (Optional) Seed the database
npx prisma db seed
```

### 5. Run the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## 📁 Project Structure

```
study-space/
├── app/                    # Next.js App Router
│   ├── (auth)/            # Authentication routes
│   ├── (dashboard)/       # Protected dashboard routes
│   ├── api/               # API routes
│   ├── globals.css        # Global styles
│   └── layout.tsx         # Root layout
├── components/            # Reusable components
│   ├── ui/               # shadcn/ui components
│   ├── forms/            # Form components
│   ├── study/            # Study-related components
│   └── layout/           # Layout components
├── lib/                  # Utility functions
│   ├── db.ts            # Database connection
│   ├── auth.ts          # Authentication config
│   └── utils.ts         # Helper functions
├── prisma/              # Database schema and migrations
│   ├── schema.prisma    # Database schema
│   └── migrations/      # Migration files
├── public/              # Static assets
└── types/               # TypeScript type definitions
```

## 🎨 shadcn/ui Components

This project uses shadcn/ui components. To add new components:

```bash
npx shadcn-ui@latest add button
npx shadcn-ui@latest add card
npx shadcn-ui@latest add input
```

Available components used in this project:
- Button, Card, Input, Label
- Dialog, Sheet, Tabs
- Table, Badge, Avatar
- Calendar, Progress, Textarea
- Toast, Alert, Skeleton

## 🗄️ Database Schema

The application uses the following main entities:

### Users
- Authentication and profile information
- Study preferences and settings

### Study Sessions
- Timer-based study sessions
- Subject categorization
- Progress tracking

### Notes
- Rich text study notes
- Tagging and categorization
- Sharing capabilities

### Flashcards
- Card-based memorization system
- Spaced repetition algorithm
- Performance analytics

### Study Groups
- Collaborative study rooms
- Member management
- Shared resources

## 🔧 Available Scripts

```bash
# Development
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint

# Database
npm run db:generate  # Generate Prisma client
npm run db:push      # Push schema to database
npm run db:migrate   # Run migrations
npm run db:seed      # Seed database
npm run db:studio    # Open Prisma Studio

# Testing
npm run test         # Run tests
npm run test:watch   # Run tests in watch mode
```

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically on every push

### Docker

```bash
# Build the image
docker build -t study-space .

# Run the container
docker run -p 3000:3000 study-space
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 Environment Setup

### Development Tools

We recommend using these tools for the best development experience:

- **VS Code** with extensions:
  - Tailwind CSS IntelliSense
  - Prisma
  - ES7+ React/Redux/React-Native snippets
  - Auto Rename Tag

### Code Style

- ESLint and Prettier are configured
- Husky for pre-commit hooks
- Conventional commits encouraged

## 🔒 Security

- Authentication handled by NextAuth.js
- API routes protected with middleware
- Database queries sanitized through Prisma
- CSRF protection enabled
- Environment variables for sensitive data

## 📊 Performance

- Next.js Image optimization
- Dynamic imports for code splitting
- Database connection pooling
- Caching strategies implemented
- Bundle analysis available

## 🐛 Troubleshooting

### Common Issues

**Database Connection Error**
```bash
# Check if PostgreSQL is running
sudo service postgresql status

# Verify connection string in .env.local
echo $DATABASE_URL
```

**Build Errors**
```bash
# Clear Next.js cache
rm -rf .next

# Reinstall dependencies
rm -rf node_modules package-lock.json
npm install
```

**Prisma Issues**
```bash
# Reset and regenerate Prisma client
npx prisma generate
npx prisma db push --force-reset
```

## 📞 Support

- 📧 Email: Nhatphanhk102@gmail.com
- 💬 Discord: [Join our community](https://discord.gg/studyspace)
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/study-space/issues)
- 📖 Docs: [Documentation](https://docs.studyspace.app)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js team](https://nextjs.org/) for the amazing framework
- [shadcn](https://twitter.com/shadcn) for the beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS
- [Prisma](https://www.prisma.io/) for the excellent database toolkit
- All contributors who help make this project better

---

Made with ❤️ by [nhaphanhk102](https://github.com/nhatphanhk)

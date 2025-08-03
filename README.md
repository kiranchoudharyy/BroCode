# BroCode Platform

This is a feature-rich, full-stack web application designed to help users practice Data Structures and Algorithms in a collaborative and competitive environment. It provides a platform where users can form groups, participate in timed coding challenges, track their progress, and even showcase their LeetCode statistics. Built with a modern tech stack, this project aims to provide a seamless and engaging experience for developers looking to hone their coding skills.

## Features

- 🔐 Authentication with Google and credentials
- 👥 Group creation and management
- 📝 DSA problem solving with Monaco editor
- 🏆 Timed coding challenges
- 📊 User progress tracking
- 🌓 Dark mode support
- 📱 Responsive design

## Tech Stack

- **Frontend**: Next.js, React, TailwindCSS, Monaco Editor
- **Backend**: Next.js API Routes
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js
- **Real-time**: Socket.io
- **Styling**: TailwindCSS, shadcn/ui

## Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn
- PostgreSQL database (or use Supabase as shown in setup)

### Environment Setup

Create a `.env` file in the root directory with the following variables:

```
# PostgreSQL Database
DATABASE_URL="postgresql://<username>:<password>@<host>:<port>/<database>?connect_timeout=300"
DIRECT_URL="postgresql://<username>:<password>@<host>:<port>/<database>?connect_timeout=300"

# Redis
REDIS_URL=redis://<host>:<port>

# NextAuth Configuration
NEXTAUTH_SECRET="<your_nextauth_secret>"
NEXTAUTH_URL=http://localhost:3000

# Google OAuth (NextAuth)
GOOGLE_CLIENT_ID="<your_google_client_id>"
GOOGLE_CLIENT_SECRET="<your_google_client_secret>"

# Judge0 API (Optional)
JUDGE0_API_KEY="<your_judge0_api_key>"
JUDGE0_API_URL=https://judge0-ce.p.rapidapi.com

# Gmail SMTP (for notifications/emails)
EMAIL_USER="<your_email_address>"
EMAIL_PASSWORD="<your_email_app_password>"

# Public URLs
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXT_PUBLIC_SOCKET_URL=http://localhost:3000

```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/kiranchoudharyy/BroCode.git
   cd brocode
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Set up the database:
   ```bash
   npx prisma migrate dev --name init
   # or if using Supabase/other cloud providers, you might need:
   npx prisma db push
   ```

4. Run the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
neetcode/
├── app/                  # Next.js app directory
│   ├── api/              # API routes
│   ├── auth/             # Authentication pages
│   ├── components/       # Reusable components
│   ├── dashboard/        # User dashboard
│   ├── groups/           # Group management
│   ├── problems/         # Problem solving
│   ├── admin/            # Admin dashboard
│   ├── lib/              # Utility functions
│   └── providers.jsx     # Context providers
├── components/           # shadcn UI components
├── prisma/               # Prisma schema and migrations
└── public/               # Static assets
```

## Deployment

This project can be deployed on platforms like Vercel, Netlify, or any other service that supports Next.js applications.

1. Set up environment variables on your hosting platform
2. Deploy using the platform's deployment process
3. Run database migrations if needed

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.

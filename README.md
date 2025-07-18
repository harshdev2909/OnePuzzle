# OnePuzzle - Daily Chess Puzzles with NFT Rewards
**[Play Now - Live Website](https://one-puzzle-fe.vercel.app/)**

**[Watch the video](https://drive.google.com/file/d/1iXyJIbPlptCCbPQef2j8xn07sIWp0QL9/view?usp=sharing)**

Experience daily chess puzzles and earn NFT rewards for your solutions!

OnePuzzle is a web application that combines chess training with blockchain technology, offering daily chess puzzles and minting successful solutions as NFTs on Solana.

![Home Page](https://github.com/aniketsahu115/OnePuzzle/blob/main/attached_assets/home%20page.png)
![Dashboard](https://github.com/aniketsahu115/OnePuzzle/blob/main/attached_assets/OnePuzzle%20Dashboard.png)
![Blog Section](https://github.com/aniketsahu115/OnePuzzle/blob/main/attached_assets/OnePuzzle%20Blog.png)



## Features

- Daily Chess Puzzles
- Interactive Chess Board
- NFT Rewards for Puzzle Solutions
- Progress Tracking Dashboard
- Learning Resources

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Shadcn/UI
- **Backend**: Node.js, Express, TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Blockchain**: Solana Web3.js
- **Development**: Vite, ESBuild

## Getting Started

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

3. Database Setup

Create a new PostgreSQL database:
```bash
create database chess_puzzle
```
Set up your database connection by creating a `.env` file:
```
DATABASE_URL=postgresql://postgres:your_password@localhost:5432/chess_puzzle
```
## Required Database Packages

```bash
npm install pg           # PostgreSQL client for Node.js
npm install drizzle-orm  # TypeScript ORM
npm install drizzle-kit  # CLI tool for Drizzle ORM
npm install dotenv       # Environment variable management
```

These packages are required for database connectivity and management:
- `pg`: PostgreSQL driver for Node.js
- `drizzle-orm`: Modern TypeScript ORM for better type safety
- `drizzle-kit`: Migration and schema management tools
- `dotenv`: Loads environment variables from .env file

Initialize the database schema:
```bash
npx drizzle-kit push
```

4. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`


## Contributing
This Project is under developement so if you want to contribute come up and develop it together!
1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## Development

```bash
# Install dependencies
pnpm install

# Start development server
pnpm dev:all

# Build for production
pnpm build
```

## Deployment

### Render Deployment

To deploy to Render, use the following configuration:

**Build Command:**
```bash
pnpm build
```

**Start Command (Option 1 - Recommended):**
```bash
./start.sh
```

**Start Command (Option 2 - Alternative):**
```bash
NODE_ENV=production node dist/server/prod.js
```

**Environment Variables:**
- `NODE_ENV=production` (required)
- `PORT` (Render will set this automatically)
- `VITE_SOLANA_RPC_URL` - Your Solana RPC endpoint
- Database connection variables (DATABASE_URL, etc.)

**Health Check URL:**
- `https://your-app.onrender.com/health`

**Important Notes:**
- The server automatically binds to `0.0.0.0` on the port provided by Render
- The production server serves static files from the `dist/public` directory
- Make sure to set `NODE_ENV=production` in your environment variables
- The server includes a health check endpoint at `/health` for monitoring

**Troubleshooting:**
- If you see "No open ports detected on 0.0.0.0", make sure you're using the production start command, not the development one
- Check the logs for any error messages during startup
- Verify that the build completed successfully before deployment

### Vercel Deployment

The project is configured for Vercel deployment with the `vercel.json` file.

## Project Structure

- `client/` - React frontend with Vite
- `server/` - Express.js backend
- `shared/` - Shared TypeScript types and schemas
- `dist/` - Production build output

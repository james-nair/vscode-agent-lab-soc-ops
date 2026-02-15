# Soc Ops  
**Break the ice, connect people, win bingo.**

Soc Ops is a social bingo game designed to make in-person mixers, team events, and networking sessions *actually fun*. Players move around the room, find people who match hilarious or thoughtful questions, and race to get 5 in a row—horizontally, vertically, or diagonally.

Perfect for icebreakers, team building, conferences, and community events.

---

## How It Works

1. **Get Your Card** — Each player starts with a unique 5×5 bingo card filled with quirky prompts
2. **Find Your People** — Mingle and find someone who matches each square ("Has lived in 3+ countries?" "Knows how to make sourdough bread?")
3. **Mark & Win** — Check off matches and get 5 in a row to win!

The game is 100% customizable—swap in your own prompts for team-specific challenges, personal questions, or event themes.

---

## Features

- **Fast Setup** — Deploy in minutes, play instantly
- **Customizable Prompts** — Tailor questions to your audience and event vibe
- **Real-Time Scoring** — Track progress and celebrate winners
- **Mobile-Friendly** — Play on phones or tablets
- **Persistent Game State** — Resume where you left off

---

## Quick Start

### Prerequisites
- [Node.js 22](https://nodejs.org/) or higher

### Run Locally
```bash
npm install
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build & Deploy
```bash
npm run build
```
Deploys automatically to GitHub Pages on push to `main`.

---

## Development

**Stack:** React 19 + Vite + TypeScript + Tailwind CSS v4

```bash
npm run lint    # Check code quality
npm run test    # Run tests
npm run build   # Production build
```

### Architecture
- `src/components/` — UI components (StartScreen, GameScreen, Board)
- `src/hooks/useBingoGame.ts` — Game state, persistence, and logic
- `src/utils/bingoLogic.ts` — Pure game logic (board generation, win detection)
- `src/data/questions.ts` — Customizable question pool

---

## Learn More

**[Follow the Lab Guide](.lab/GUIDE.md)** for detailed instructions on setup and customization.

Check out [CONTRIBUTING.md](CONTRIBUTING.md) to contribute ideas, questions, or improvements.

---

## License

MIT — Use and customize freely!

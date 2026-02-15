# Copilot / AI Agent Instructions  Soc Ops

- [ ] `npm run lint`
- [ ] `npm run build`
- [ ] `npm run test`

Quick snapshot: React + Vite + TypeScript app (Tailwind v4).
Key dirs: `src/components`, `src/hooks`, `src/utils`, `src/data`.

Commands
- Dev: `npm install` then `npm run dev`  http://localhost:5173/
- Build: `npm run build` (runs `tsc -b` then `vite build`)
- Tests: `npm run test` (Vitest)
- Lint: `npm run lint` (ESLint)

Architecture & patterns
- UI: presentational components in `src/components` (minimal logic).
- Game state: `src/hooks/useBingoGame.ts` holds state, persistence, and side-effects.
- Pure logic: `src/utils/bingoLogic.ts` (board generation, toggle, bingo detection) with tests in `src/utils/bingoLogic.test.ts`.
- Data: static pool in `src/data/questions.ts`. Board is 5x5; center is free space at index 12.
- Persistence: `localStorage` key `bingo-game-state`, `STORAGE_VERSION = 1`. If changing persisted shape, bump version and add a migration in `loadGameState()`.

Quick guidelines for edits
- Move behavior into `useBingoGame` or `bingoLogic.ts`; keep components dumb.
- When changing rules, update both logic and tests (`getWinningLines()` and tests).
- For UI changes, follow `StartScreen.tsx` / `GameScreen.tsx` patterns: callbacks from `useBingoGame`.

Files to inspect first
- `src/utils/bingoLogic.ts`
- `src/hooks/useBingoGame.ts`
- `src/data/questions.ts`
- `src/components/StartScreen.tsx`, `src/components/GameScreen.tsx`

Note: No external APIs. Run `npm run test` and `npm run build` before creating PRs.

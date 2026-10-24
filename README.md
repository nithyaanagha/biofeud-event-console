# BioFeud: Where Science Meets Society

An offline-capable host console for a live biotechnology game show. BioFeud includes two rounds: a ten-question answer-board game and five Hot Takes presentations with audience questions.

## Requirements

- Node.js 18 or newer
- npm (included with Node.js)

There are no third-party package dependencies. Event state is saved in the browser's local storage; the core game does not require an internet connection.

## Install and run

From this folder, start the local server:

```sh
npm start
```

Open the local URL printed in the terminal (by default, `http://127.0.0.1:4173`). To use another port, set the `PORT` environment variable before running `npm start`.

Check the JavaScript syntax and required app files with:

```sh
npm run build
```

## Host quick start

1. Replace the sample team names, set colours, and add or remove teams in **Team line-up**.
2. Choose **Start / resume event**. Questions are assigned in order across the registered teams and can be reassigned on each board.
3. Start the two-minute timer. Reveal each matching answer tile once to award its points. Use **Strike** for an incorrect answer; the second strike ends the turn and opens the audience buzzer. The host judges spoken answers.
4. A correct audience answer earns the configured bonus. An incorrect answer has no score deduction. Reset the buzzer if the host allows another attempt.
5. Round 1 scores determine the presenting finalists. If there is a tie for the fifth slot, choose the finalist on the Round 1 scoreboard.
6. In **Hot Takes**, assign topics, run the 15-minute preparation timer, then start each 60-second opening statement. Confirm the first two eligible questioners, mark each spoken question, and run the shared 45-second answer timer.
7. Enter and save presenter and questioner rubric scores separately. Round 1 points carry forward, and all teams can win through question points.

## Host controls

- **Space** starts or pauses the timer for the section in view.
- **S** applies a strike and **B** opens the audience buzzer on a BioFeud board.
- **N** advances to the next BioFeud question.
- **H** opens Host Controls; **Esc** closes the drawer or a dialog.
- Host Controls lets you edit point values and the current answer board, correct scores, enable or disable audience buzzing, and import or export event JSON.
- **Restart event** clears scores and progress but keeps team names and colours. **Reset all event data** clears the entire local session.

Keep the same browser profile for the event so its saved session remains available. Export the event JSON before the event as a recovery copy.

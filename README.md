# Stop Signal

Watch an AI agent decide when to stop, token by token.

**https://wheel-is.github.io/stop-signal/**

An agent (Qwen3-4B) gets a small job and four tools. It calls one tool at a time, reads each
result, and at some point writes a final answer. Every word is coloured by a score read from
inside the model at that moment: blue when its next turn will call another tool, orange when
its next turn will be the final answer.

- **Recorded runs** play for anyone: four tasks, each at three settings of the push dial.
- **Live runs** need a passcode. The agent then runs on a GPU on a fresh task each time, and
  the dial pushes it to stop sooner or keep going.

The score is a linear read-out of the model's layer 24. The push adds one direction to its
layer 23. Both come from a study of what makes a tool-calling agent stop.

This repository holds only the page (`index.html`) and the recorded runs (`runs.json`).

# Token Meter

A single-page tool that shows how many tokens your AI chat uses while you chat.

Paste your prompt and the AI's reply. Token Meter shows:

- **Tokens per message**, counted live as you type
- **How full the context window is**, split into app overhead, your messages and AI replies
- **Tokens and turns left** before the model runs out of room
- **Your usage budget**: set your own limit and see what each message costs
- **Tokens per turn chart**: every message re-sends the whole chat, so each turn costs more than the last
- **Image cost estimate** from the image's pixel size
- **Tips** for making tokens last

## Use it

Open `index.html` in any browser, or visit the GitHub Pages site for this repo. No install or build step needed.

## Accuracy

- **ChatGPT / GPT-4o**: exact counts, using OpenAI's `o200k_base` tokenizer via [gpt-tokenizer](https://github.com/niieani/gpt-tokenizer).
- **Claude and Gemini**: estimates scaled from that tokenizer (marked with ≈), because they don't publish a browser tokenizer.
- Paid chat apps don't publish their limits in tokens, so the context window, hidden overhead and budget can all be edited.

Your chat stays in your browser (localStorage). Nothing is sent anywhere.

## License

MIT

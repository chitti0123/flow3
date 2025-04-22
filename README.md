#Flow3 Auto Task Bot

An automated task completion bot for Flow3 platform that helps manage multiple accounts, automatically claim tasks, and track point earnings. This tool is designed to simplify the Flow3 airdrop farming process.

## Features

- ✅ Multi-token support - manage multiple Flow3 accounts from a single tool
- 🌐 Proxy support - rotate through proxies to avoid rate limits
- 💰 Point tracking - view your current point balance and earnings rate
- 🚀 Automatic task claiming - completes all available tasks automatically
- ⏱️ Continuous operation - runs in cycles, automatically checking for new tasks
- 🔄 Auto-reload - reloads tokens and proxies without restarting

## Installation

1. Clone the repository:
```bash
git clone https://github.com/airdropinsiders/Flow3-Auto-Task.git
```

2. Navigate to the project directory:
```bash
cd Flow3-Auto-Task
```

3. Install dependencies:
```bash
npm install
```

## Configuration

### Setting up tokens

Create a file named `token.txt` in the project root directory. Add your Flow3 authorization tokens (one per line):

```
your_first_token_here
your_second_token_here
your_third_token_here
...
```

To get your token:
1. Log in to [Flow3](https://app.flow3.tech/)
2. Open your browser's developer tools (F12)
3. Go to the Network tab
4. Refresh the page and look for any API request
5. Find the "authorization" header in the request headers
6. Copy the token value (without "Bearer ")

### Setting up proxies (optional)

Create a file named `proxies.txt` in the project root directory. Add your proxy strings (one per line):

```
username:password@ip:port
ip:port
http://username:password@ip:port
```

## Usage

Start the bot with:

```bash
node index.js
```

The bot will:
1. Load your tokens and proxies
2. Process each token in sequence
3. Fetch and claim all available tasks
4. Display point statistics for each account
5. Wait for a configurable amount of time
6. Repeat the process in a continuous loop

## Output Example

```
----------------------------------------
  FLOW3 AUTO TASK - AIRDROP INSIDERS  
----------------------------------------

✅ Loaded 3 tokens successfully from token.txt
🌐 Loaded 2 proxies from proxies.txt
🚀 Starting Flow3 Multi-Token Task Bot...

⏱️ Starting cycle #1
--------------------------------------------------

🔑 Processing Token #1
🌐 Using proxy: username:password@127.0.0.1:8080
ℹ️ Found 5 tasks for token #1
ℹ️ Processing: Daily Check-in (idle ⏳) - 5 points
✅ Task 612a8f3c4d9e7b1a2c3d4e5f claimed successfully!
...

💰 BALANCE INFORMATION (TOKEN #1) 💰
------------------------------------------
⭐ Total Points:         275.00
✓ Task Points:          250.00
🚀 Internet Points:      20.00
ℹ️ Referral Points:      5.00
⏱️ Today's Earnings:     25.00
💰 Earning Rate:         20.00/day
------------------------------------------
```

## Requirements

- Node.js v16.x or later
- NPM v8.x or later

## Dependencies

- axios - HTTP client for API requests
- https-proxy-agent - For proxy support
- fs - For file operations
- path - For file path manipulation

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Disclaimer

This tool is provided for educational purposes only. Please use responsibly and in accordance with Flow3's terms of service. The developers are not responsible for any misuse or account suspensions resulting from the use of this tool.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, join our [Discord server](https://discord.gg/airdropinsiders) or open an issue on GitHub.

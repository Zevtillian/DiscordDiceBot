# DiscordDiceBot
A discord bot designed for rolling dice for Dungeons and Dragons
README for Dice Rolling Bot

---

## Overview
This is a simple Discord bot written in Python that allows users to roll dice in the format commonly used in Dungeons and Dragons (D&D). The bot supports standard dice types (`d4`, `d6`, `d8`, `d10`, `d12`, `d20`, and `d100`) and has an easter egg for rolling a "fireball" (8d6). It also limits the number of dice you can roll to prevent abuse.

---

## Features
1. **Roll Dice**: Roll up to 300 dice of valid types (`d4`, `d6`, `d8`, `d10`, `d12`, `d20`, `d100`).
2. **Easter Egg**: Typing `!roll fireball` rolls `8d6`.
3. **Error Handling**:
   - Validates dice format (e.g., `2d6`, `10d20`).
   - Ensures dice type is valid.
   - Limits the number of dice rolled to a maximum of 300.

---

## Requirements
To run this bot, you need the following:
- Python 3.8+
- The following Python packages:
  - `discord.py`
  - `nest_asyncio`

Install these packages with:
```
pip install discord.py nest_asyncio
```

---

## Setup and Installation
1. **Clone or Download the Code**:
   - Save the code into a Python file, e.g., `dice_bot.py`.

2. **Get a Discord Bot Token**:
   - Log in to the [Discord Developer Portal](https://discord.com/developers/applications).
   - Create a new application.
   - Go to the **Bot** section, click **Add Bot**, and copy the **Bot Token**.

3. **Configure Bot Permissions**:
   - Go to the **OAuth2** tab and select the following permissions:
     - **Bot Permissions**: Check `Send Messages`, `Read Messages`, and `Use Slash Commands`.
   - Copy the generated OAuth2 URL and add the bot to your server.

4. **Add the Token to the Code**:
   - Replace `YOUR_BOT_TOKEN_HERE` in the code with your bot token:
     ```python
     bot.run("YOUR_BOT_TOKEN_HERE")
     ```

5. **Run the Bot**:
   - Run the Python script:
     ```bash
     python dice_bot.py
     ```
   - The bot will come online and print a message like:
     ```
     Bot is online as Dice Goblin#1624!
     ```

---

## Commands
Here are the commands supported by the bot:

1. **Roll Dice**:
   - Format: `!roll NdX`
     - `N`: Number of dice (1–300).
     - `X`: Type of dice (e.g., 4, 6, 8, 10, 12, 20, 100).
   - Example:
     - `!roll 2d6` → Rolls 2 six-sided dice.
     - Output: 🎲 Rolls: [3, 5] | Total: 8

2. **Fireball Easter Egg**:
   - Command: `!roll fireball`
   - Rolls `8d6` for a fireball spell.
   - Example:
     - Output: 🎲 Rolls: [4, 6, 1, 5, 3, 6, 4, 2] | Total: 31

3. **Ping Command**:
   - Command: `!ping`
   - Example:
     - Output: Pong!

---

## Error Handling
The bot will respond with an error message for invalid input:
1. Invalid Dice Format:
   - Input: `!roll 2d`
   - Output: "Invalid dice format! Use NdX (e.g., 2d6)."

2. Invalid Dice Type:
   - Input: `!roll 1d3`
   - Output: "Invalid dice type! Choose from: d4, d6, d8, d10, d12, d20, d100."

3. Exceeding Dice Limit:
   - Input: `!roll 400d6`
   - Output: "You can roll between 1 and 300 dice."

---

## Notes
- **Compatibility**: This bot has been tested only in Jupyter Lab. It may not work in other Python environments without modification. If you encounter issues, consider running it in Jupyter Lab or adapting the code to your environment.

---

## Contributing
Feel free to suggest new features or report bugs. You can fork the repository, make changes, and submit a pull request.

---

## License
This project is open-source and available under the MIT License.

---

With this bot, you can spice up your D&D sessions on Discord! 🎲 Enjoy!

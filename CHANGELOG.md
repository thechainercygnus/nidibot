# Changelog

All notable changes to this project will be documented in this file.

## [1.0.1] - 2024-09-03

### .gitignore

- Corrected folder filter.

### 🚀 Features

- *(cd)* Added usage of git-cliff GitHub Action.
- *(bots)* Controlling notify period from nidibot configuration.

### 🐛 Bug Fixes

- *(ci)* Fixed generation of CHANGELOG.md and GitHub release entry.
- *(bots)* Fixed issue with crash when there were no backups available.
- *(telegram-bot)* Dropping pending signals from Telegram server for avoiding spam on nidibot restart.
- *(telegram-bot)* Fixed issue when conversation was not started again after one run.
- *(ci)* Corrected way of generating CHANGELOG.md and GitHub release entry text.
- *(telegram-bot)* Resizing reply keyboard during backup_restore.
- *(telegram-bot)* Fixed anomalous slashes in strings.
- *(ci)* Corrected creation of GitHub release entry text.
- *(server_provider_factory)* Removed incorrect return type.
- *(nidibot)* Fixed incorrect import from nidibot package.
- *(discord-bot)* Fixed crash during call of backup_restore when amount of backups was higher than 25.

### 🚜 Refactor

- *(bot_factory.py)* Changed support bot list to be a static private class field.
- *(server_provider_factory.py)* Changed supported server provider list to be a static private class field.
- *(bot-base)* Renamed BotInterface to BotBase.
- *(telegram-bot)* Switched fallback to MessageHandler and not CommandHandler.
- *(telegram-bot)* Changed status command handling to ConversationHandler.
- *(telegram-bot)* Changed start command handling to ConversationHandler.
- *(telegram-bot)* Changed stop command handling to ConversationHandler.
- *(telegram-bot)* Changed restart command handling to ConversationHandler.
- *(telegram-bot)* Changed backup_create command handling to ConversationHandler.
- *(telegram-bot)* Changed backup_list command handling to ConversationHandler.
- *(bots)* Moved emojis to BotBase class.
- *(telegram-bot)* Unified common commands under the same functionality.
- *(telegram-bot)* Unified conversation enumeration.

### 📚 Documentation

- *(nidibot)* Added docstrings.
- *(server_providers)* Added docstrings.
- *(bots)* Added docstrings.
- *(README.md)* Corrected mentions of package import.
- *(README.md)* Added nidibot configuration description.
- *(README.md)* Added information about 25 button limitation of Discord for backup_restore command.

### 🧪 Testing

- Removed due to being redundant.

### ⚙️ Miscellaneous Tasks

- *(discord-bot)* Added missing imports.
- *(nidibot)* Removed unused import.
- *(nidibot)* Set default parameter values in GeneralConfiguration.
- *(tests)* Removed redundant test files and classes.
- *(setup.cfg)* Changed development status to Production/Stable.

### README.md

- Added description and commands.
- Added information about limitations.
- Corrected typos.
- Added entry about '/backup_restore'.
- Removed limitation entry about only one Telegram bot.

### Bot_interface.py

- Moved common functionality from discord_bot.py and telegram_bot.py.

### Build

- *(deps)* Bump actions/setup-python from 3 to 5
- *(deps)* Bump actions/checkout from 3 to 4

### Discord_bot.py

- Fixed issue with showing backup list.
- Removed redundant smileys.

### Game_server.py

- Added GameServer wrapper class for easier access and control of each game server instance.
- Added docstrings.

### Nidibot.py

- Added descriptions to all commands.
- Fixed double stating of @command decorator.
- Added on_ready() event.
- Migrated bot to hikari + lightbulb. That fixed issue with commands not showing in Discord chat.
- Changed structure of bot_configuration.json for higher flexibility.
- Properly initializing server providers.
- Added test options for each available command.
- Switched to using NitradoServerProvider class.
- Added server information into response.
- Added nidibot version into logging.
- Added possibility to state server name in all available commands.
- Added server address to response title.
- Moved bot functionality to separate folder. Implemented factory and interface classes for server providers.
- Modifying working directory in nidibot.service file upon copy.

### Nidibot/templates

- Corrected errors.

### Nitrado.py

- Added safety checks in constructor.

### Nitrado_server_provider.py

- Removed excessive logging.
- Moved some variables to base class.
- Added API check, MySQL credentials reading and saving MySQL DB via mysqldump.

### Server_provider_interface.py

- Accessing game server functions via IDs rather than indices.

### Setup.cfg

- Corrected format of install_requires.
- Added missing ftputil.
- Corrected development status, environment and intended audience.
- Added missing python-telegram-bot[job-queue] dependency.

### Telegram_bot.py

- Fixed redundant logging of httpcore logger.
- Disabled redundant logging.
- Added auto notification for channels from allowed_channels list.
- Fixed issue with running in thread.

<!-- generated by git-cliff -->

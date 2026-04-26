# WoW TCG Card Database

A modular, YAML-based database for the World of Warcraft Trading Card Game.
  
> [!IMPORTANT]
> The structural foundation of this database is complete. Every card printing and card oracle has a dedicated file. However, ~90% of the actual game properties (rules text, costs, abilities) are incomplete. Editors are active collaborating on this data and welcome community contributions to help finish the data!
  

## 🃏 Structure

During the build process, the compilation script merges the project's individual YAML files into flat, fully-realized JSON objects.

- `data/card/`: **Physical Printings.** Properties specific to an exact card (artist, flavor text, set number). 
- `data/oracle/`: **Consistent Properties.** The card's core mechanics that remains identical across all reprints (cost, class, abilities). 
- `data/set/`: **Release Data.** Set releases. Cards inherit set properties during build.
- `data/collection/`: **Macro-Groupings.** Broader buckets (like blocks or eras) that group multiple sets together.
- `data/format/`: **Card Legality.** Standalone rules defining allowed sets, and specific card bans/restrictions. 
- `data/deck/`: **Pre-constructed Lists.** Official product decklists (Starter Decks, Raid Decks) mapping card IDs to quantities.
- `schema/`: **Validation Blueprints.** Strict Schemas to automatically validate contributions.
- `script/`: **Build Pipeline.** Python utilities that compile the individual YAML files into final distribution formats.
- `dist/`: **Distribution Directory.** The final, compiled files. *(Note: This folder is git-ignored. Editors not running the build script locally can instead access these files from the Releases page).*
  

## 🐍 Scripts

- `python script/compile.py`: Validates all source YAMLs and generates the joined JSON database in `dist/`.
- `python script/split.py`: (Optional) Re-generates the modular YAML structure from the joined JSON files.
  

## 🐝 Community & Contributing

This database relies on community contributions to stay accurate and up-to-date. You are invited to contribute if you spot a missing card, a typo in rules text, incorrect set data, etc.

*   **Read the Docs:** Before editing any YAML files, please read the wiki (coming soon).
*   **[Join Discord](https://discord.gg/b8Se3B9Cb4):** Discuss structure and data accuracy.

## 🪩 Featured Apps

Here are a few projects currently using this database in production. 

*If you have built an app, simulator, or tool using this data, please share on Discord!*

*   **[CardCarp](https://cardcarp.com)** - A companion web-app to showcase all TCGDB cards. 
  

## 🐲 Support the Project

If TCGDB saved you 100 hours of typing out card text, please consider a Patreon Membership. 
  

[![Patreon](https://img.shields.io/badge/Patreon-FF424D?style=for-the-badge&logo=patreon&logoColor=ffffff&label=%20&labelColor=000000)
](https://www.patreon.com/c/tcgdb)
  
  

⚖️ Legal Disclaimer

-# Card data and images are provided strictly for educational study, historical preservation, and personal, non-commercial use.

-# All trademarks, copyrights, and artwork remain the exclusive property of their respective rights holders. This is an independent, community-driven project and is not affiliated with, endorsed by, sponsored by, or connected to any publisher or intellectual property owner.

-# The underlying code/schemas are MIT licensed, granting full rights to use, modify, and redistribute.
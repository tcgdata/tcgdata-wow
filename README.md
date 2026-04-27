# WoW TCG Card Dataset 👹

An open, flat-file dataset for the World of Warcraft Trading Card Game.

<br>
  
> [!IMPORTANT]
> The structural foundation of this dataset is complete.<br> Every card printing and card oracle has a dedicated file.<br>
> However, much of the actual game properties (rules text, costs, abilities) are incomplete.<br>
> Editors are actively collaborating on this data and welcome community contributions.

<br>

## 🃏 Structure

During the build process, the compilation script merges the project's individual YAML files into flat, fully-realized JSON objects.

- `data/card/`: **Physical Printings.** Properties specific to an exact card (artist, flavor text, set number).<br>
  
- `data/oracle/`: **Consistent Properties.** The card's core mechanics that remains identical across all reprints (cost, class, abilities).<br> 
  
- `data/set/`: **Release Data.** Set releases. Cards inherit set properties during build.<br>
  
- `data/collection/`: **Macro-Groupings.** Broader buckets (like blocks or eras) that group multiple sets together.<br>
  
- `data/format/`: **Card Legality.** Standalone rules defining allowed sets, and specific card bans/restrictions.<br>
  
- `data/deck/`: **Pre-constructed Lists.** Official product decklists (Starter Decks, Raid Decks) mapping card IDs to quantities.<br>
  
- `schema/`: **Validation Blueprints.** Strict Schemas to automatically validate contributions.<br>
  
- `script/`: **Build Pipeline.** Python utilities that compile the individual YAML files into final distribution formats.<br>
  
- `dist/`: **Distribution Directory.** The final, compiled files. *(Note: This folder is git-ignored. Editors not running the build script locally can instead access these files from the Releases page).*

<br>
  

## 🐍 Scripts
 
- `python script/compile.py`: Validates all source YAMLs and generates the joined JSON in `dist/`.<br>
  
- `python script/split.py`: (Optional) Re-generates the modular YAML structure from the joined JSON.

<br>  
  

## 🐝 Community & Contributing

This dataset relies on community contributions to stay accurate and up-to-date. You are invited to contribute if you spot a missing card, a typo in rules text, incorrect set data, etc.

*   **Read the Docs:** Before editing any YAML files, please read the wiki (coming soon).<br>  
  
*   **[Join Discord](https://discord.gg/b8Se3B9Cb4):** Discuss structure and data accuracy.

<br>

## 🪩 Featured Apps

Here are a few projects currently using this dataset in production. (*If you have built an app, simulator, or tool using this data, please share on Discord!*)

*   **[CardCarp](https://cardcarp.com)** - A companion web-app to showcase all TCGData. 

<br>  
  

## 🐲 Support the Project

Please consider a Patreon Membership if TCGData saved you 100 hours of manual data entry.

*   **[TCGData on Patreon](https://www.patreon.com/cw/tcgdata)**

  
<br>    
  
## ⚖️ Legal Disclaimer

<sub>Card data and images are provided strictly for educational study, historical preservation, and personal, non-commercial use.</sub>

<sub>All trademarks, copyrights, and artwork remain the exclusive property of their respective rights holders. This is an independent, community-driven project and is not affiliated with, endorsed by, sponsored by, or connected to any publisher or intellectual property owner.</sub>

<sub>The underlying code/schemas are MIT licensed, granting full rights to use, modify, and redistribute.</sub>

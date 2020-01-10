# PlayHome Translations
English translation project for PlayHome.

The translations are applied at runtime and do not require replacing or modifying any game files.

## Installation
1. Install at least [BepInEx 5 5.0.1](https://github.com/BepInEx/BepInEx), latest [BepisPlugins for PlayHome](https://github.com/bbepis/BepisPlugins/releases) and the latest [XUnity.AutoTranslator](https://github.com/bbepis/XUnity.AutoTranslator).
2. Go to the releases page above and download the latest release. Alternatively, advanced users can get the latest beta translations by clicking "Clone or download" button above. Read the ADV translations section below to see how to enable ADV translations if you do this.
3. Extract the zip and merge the Translation folder with the one in your BepInEx folder. It's recommended to delete your old translation folder to prevent translation collisions.

## Contribution
Any help is appreciated. Regardless of your translation skill and Japanese knowledge you can still help with translations. Even if you have no experience you can help by proofreading or using Google translate or other translation services and then cleaning up the translation using sanity and a bit of logic. Absolutely no raw machine translations will be accepted, users can use [XUnity.AutoTranslator](https://github.com/bbepis/XUnity.AutoTranslator/releases) for that.

Translations are all inside of `Bepinex\Translation\en\` folder. They are then split into three folders:
- `Text` - Normal text replacements and modifications.
- `Texture` - Image replacements.
- `RedirectedResources` - Replacements for entire text assets. Used for ADV translations because of better organization and performance.

Coordinate with other translators on the [Illusion Soft Discord server](https://discord.gg/illusionsoft) #translation channel. To avoid translation conflicts please ask if anyone is working on a file. If you have any questions about the quality of your translations, ask for advice on the server.

### How to add or improve translations
- If you want to make a simple edit simply open the file in question and click edit. After you are done editing, commit the changes and stall a pull request.
- If you have more translations to submit [fork the repository](https://help.github.com/articles/fork-a-repo/). Upload your changes to your fork and then [submit a pull request](https://help.github.com/articles/about-pull-requests/). Your pull request will be reviewed and accepted after a quality check. Again, no raw machine translations will be accepted. Proper capitalization, punctuation, and spelling is a must.

### ADV translations
Every translation.txt file has the raw Japanese text that needs translations. Each one starts commented out (`//` at the begining) so it will not be loaded. For your text to display correctly in game, put the translation on the right side of the equal sign and remove the `//` at the start of the line. Do not edit the Japanese text or the translation will not work.

The `abdata` folder inside of `Bepinex\Translation\en\RedirectedResources\assets` can be compressed into a .zip archive to be read by the game (simply right-click on the abdata folder and then compress to .zip). Uncompressed files under abdata are also still loaded. The game has to be restarted in order to see updated translations.

#### Format strings

Format strings have replacements in them processed by [`String.Format`](https://docs.microsoft.com/en-us/dotnet/api/system.string.format?view=netframework-4.6#Starting).  The sections that are replaced by the game engine will look like `{0}`, `{1}`, `{2}`, etc.  Usually they are a character name or the name of some item.  The same replacements found in the original string should exist in the translated string.

Example:
```
{0}と仲がいいと思ってるわ=I think I'm good friends with {0}.
```

### Tools
[Yomichan](https://foosoft.net/projects/yomichan/)  
This browser plugin allows you to see the definition of Japanese words by putting your mouse over them in the browser and pressing shift.  

Dictionaries:  
https://jisho.org/  
http://www.romajidesu.com/  

### Original UITranslation
Kenzato#2582 ([Patreon](https://www.patreon.com/Kenzato))
Aria#1551 (???)

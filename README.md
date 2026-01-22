# Better colors for default implementation of Firefox groups

![stylesheet preview](/image.png)
This repository contains just a `userChrome.css` file that overwrites some Firefox variables to make groups look better with dark/black themes.

Changes in my own stylesheet (that sits in repository under `./userChrome.css`) only affect `--tab-group-color-{NAME}-pale` to make the background darker than the text, instead of eye-blasting white.

Variable names were extracted using the browser toolbox, and some variable usage looks strange, tbh.

Currently, I can say that:
* Names of available colors are presented as: `green`, `red`, `blue`, `orange`, `purple`, `cyan`, `yellow`, `pink`, and `gray` (these are the names Mozilla uses in variable names).
* Any of `--tab-group-color-{NAME}`:
  * *MINIMIZED*: foreground and outline
  * *EXPANDED*: background
* Any of `--tab-group-color-{NAME}-pale`:
  * *MINIMIZED*: background
  * *EXPANDED*: foreground
* Any of `--tab-group-color-{NAME}-invert`:
  * I found the use of this only in vertical tabs when a tab is expanded. In that case, this color is used as a background. Maybe this color is used somewhere else in the tab engine, but I have not found it.

---

# INSTALLATION

1. First, type `about:config` in the address bar and open it. 
2. Find `toolkit.legacyUserProfileCustomizations.stylesheets` (just paste this into the search box) and set it to **true**. This is required if you want Firefox to read custom styles from `userChrome.css`.
3. Now, you need to open `about:profiles`. There will be a profile with: `This is the profile in use and it cannot be deleted.` That's the one you are using.
4. Navigate to the path under **"Root Directory"**, create a folder named `chrome`, and move `userChrome.css` inside.
5. Restart Firefox and everything should work. If not — ask AI for assistance, lol.

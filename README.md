AFK HALLOW'S EVE SCRIPT - Fish an Anime RNG (Roblox)
====================================================

WHAT IT DOES
  - Hallow's Eve: while the event is on, it holds the character in hotbar slot 2.
    When that character gets the Dracula mutation, it moves on to slot 3, then 4...
    and stops when it reaches a potion slot. When the event ends, it puts the
    character away.
  - Selene's shop: when Selene's prompt shows up, it opens her shop and buys every
    item that costs cash or gems. It skips items that say OUT OF STOCK or OWNED.
  - Auto rebirth: once an hour it opens the rebirth menu and presses Rebirth!.
    If you don't have enough cash, it closes the "Skip Rebirth" Robux pop-up.
  - It NEVER spends Robux. Robux buttons and Roblox's Buy button are never clicked.


SETUP (one time)
  1. Double-click install_requirements.bat (installs Python, the packages and
     Tesseract OCR). If Windows says "Windows protected your PC", click
     More info -> Run anyway.
  2. Keep afk_hallows_eve.py in the same folder.


BEFORE YOU RUN IT
  - Screen must be 1920x1080, with Roblox full-size (like fullscreen).
  - Start Roblox from the normal Play button (the window must be called "Roblox").
  - Put your Hallow's Eve character in hotbar slot 2, any other characters right
    after it (slots 3, 4...), and potions after those.
  - For Selene: stand where her "Selene's Store / Talk" prompt appears when she spawns.


HOW TO RUN
Open the folder, click the address bar, type  cmd  and press Enter.
Then type one of the commands below and press Enter.

  Normal use:
    python afk_hallows_eve.py                  Everything: Hallow's Eve + Selene + rebirth

  Toggles (choose what runs):
    python afk_hallows_eve.py --hallows-only   Only Hallow's Eve (no Selene shop)
    python afk_hallows_eve.py --shop-only      Only Selene's shop (no Hallow's Eve)
    --no-rebirth                               Add to any command to turn off auto rebirth
                                               e.g.  python afk_hallows_eve.py --shop-only --no-rebirth

  Test tools (run once, then exit):
    python afk_hallows_eve.py --sample         Checks it reads the event and hotbar correctly.
                                               Saves debug_*.png pictures you can look at.
    python afk_hallows_eve.py --mutation-sample [word]
                                               Shows what it reads above your characters
                                               (e.g. --mutation-sample dracula).
    python afk_hallows_eve.py --shop-sample    With Selene's shop OPEN: shows which buttons it
                                               would click and what it reads for stock.
                                               Saves debug_shop.png and debug_close.png.
    python afk_hallows_eve.py --shop-now       Runs one Selene shop visit right now.
    python afk_hallows_eve.py --rebirth-now    Tries one rebirth right now.


HOW TO STOP
  Press Ctrl+C in the black window, or quickly move your mouse into a corner of
  the screen (emergency stop).


SETTINGS (optional - open afk_hallows_eve.py in Notepad, near the top)
  FIRST_SLOT = 2           Hotbar slot of your first Hallow's Eve character
  MUTATION_WORD = "dracula" Mutation to wait for before moving to the next slot
  REBIRTH_EVERY = 60 * 60  Seconds between rebirth checks (60*60 = 1 hour)
  BUY_CLICKS = 10          Max clicks per shop item
  STOCK_CHECK = True       Stop clicking items that say OUT OF STOCK (False = off)
  AUTO_FOCUS = True        Brings Roblox to the front before pressing keys
  TESSERACT_PATH           Where Tesseract OCR is installed (leave as is normally)


GOOD TO KNOW
  - Don't use the mouse while it's shopping or rebirthing (about 10-60 seconds).
  - At 250 rebirths (when SACRIFICE unlocks) auto rebirth stops by itself, so you
    can choose yourself.
  - Using macros can be against Roblox's rules. Use at your own risk.

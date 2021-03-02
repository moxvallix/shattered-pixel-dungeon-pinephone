# Shattered Pixel Dungeon

## Info about this fork
This is a fork of the regular Shattered Pixel Dungeon, but with some slight tweaks to make it work with Linux ARM devices (Made for and tested on the PinePhone).
Regular Shattered Pixel Dungeon uses libGDX version 1.9.10, but Linux ARM support was added to libGDX in version 1.9.12. The file build.gradle was updated to change the game to use 1.9.12. However, this then created an issue in the file `shattered-pixel-dungeon-pinephone/SPD-classes/src/main/java/com/watabou/input/InputHandler.java`, with the code block: 
	
	@Override
	public boolean scrolled(int amount) {`
		ScrollEvent.addScrollEvent( new ScrollEvent(pointerHoverPos, amount));
		return true;
	}

For now, I just commented out that code block, and the game compiled and ran properly. The code seemed to be related to scrolling in some sense. Obviously it's not great to just comment out code rather than fix it, but hey, I'm not a Java developer.

The game runs well, but it is recommended that you set the game to fullscreen to play.

## The regular spiel
A Roguelike RPG, with randomly generated levels, items, enemies, and traps! Based on the [source code of Pixel Dungeon](https://github.com/00-Evan/pixel-dungeon-gradle), by [Watabou](https://www.watabou.ru).

Shattered Pixel Dungeon currently compiles for Android and desktop platforms. It is available from [GitHub](https://github.com/00-Evan/shattered-pixel-dungeon/releases), [Google Play](https://play.google.com/store/apps/details?id=com.shatteredpixel.shatteredpixeldungeon), [Amazon](https://www.amazon.com/Shattered-Pixel-Dungeon/dp/B00OH2C21M), and [F-Droid](https://f-droid.org/repository/browse/?fdid=com.shatteredpixel.shatteredpixeldungeon).

If you like this game, please consider [supporting me on Patreon](https://www.patreon.com/ShatteredPixel)!

There is an official blog for this project at [ShatteredPixel.com](http://www.shatteredpixel.com).

The game also has a translation project hosted on [Transifex](https://www.transifex.com/shattered-pixel/shattered-pixel-dungeon/).

Note that **this repository does not accept pull requests!** The code here is provided in hopes that others may find it useful for their own projects, not to allow community contribution. Issue reports of all kinds (bug reports, feature requests, etc.) are welcome.

If you'd like to work with the code, you can find the following guides in `/docs`:
- [Compiling for Android.](docs/getting-started-android.md)
    - **[If you plan to distribute on Google Play please read the end of this guide.](docs/getting-started-android.md#distributing-your-apk)**
- [Compiling for desktop platforms.](docs/getting-started-desktop.md)
- [Recommended changes for making your own mod.](docs/recommended-changes.md)

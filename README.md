# apple-music-discord-rpc

**[Deno](https://deno.land) + JavaScript for Automation (JXA) Discord Rich Presence Client for the macOS Apple Music app (Catalina and later) and legacy iTunes.**

Works with local tracks and Apple Music streaming service.

## Features

- Can be launched in background at login.
- No status bar icon clutter.
- Presence is only enabled when actually playing something.
- Displays album artworks and links to Apple Music (when possible) ([#5](https://github.com/NextFire/apple-music-discord-rpc/pull/5)).
- Spotify search button ([#59](https://github.com/NextFire/apple-music-discord-rpc/pull/59)).

<img width="370" src="https://hikari.butaishoujo.moe/p/545608d1/Capture%20d’écran%202023-04-26%20à%2010.49.08.png">

## Getting Started

Choose one of the two methods below to install the script and enable the macOS launch agent that starts it on login.

### Homebrew (Recommended)

#### Install

After installing [Homebrew](https://brew.sh), execute the following commands:

```
brew tap nextfire/tap
brew install apple-music-discord-rpc
brew services restart apple-music-discord-rpc
```

These commands

- add [this tap](https://github.com/NextFire/homebrew-tap) to Homebrew,
- install its `apple-music-discord-rpc` formula (and Deno),
- enable the launch agent and start it immediately.

The `music-rpc.ts` executable is now also in `PATH`.

#### Uninstall

```
brew services stop apple-music-discord-rpc
brew remove apple-music-discord-rpc
brew untap nextfire/tap
```

### Shell Scripts

#### Install

Install [Deno](https://deno.land), clone the repository and execute [`install.sh`](/scripts/install.sh):

```
git clone https://github.com/NextFire/apple-music-discord-rpc.git
cd apple-music-discord-rpc/
./scripts/install.sh
```

It will copy the [launch agent](/scripts/moe.yuru.music-rpc.plist) into `~/Library/LaunchAgents/` and edit it accordingly.

#### Uninstall

```
cd apple-music-discord-rpc/
./scripts/uninstall.sh
cd ../
rm -rf apple-music-discord-rpc/
```

# ani-cli

> Working on macOS Monterey v12.0
> Must install 'util-linux' with Homebrew for this to work

A cli to browse and watch anime.

This tool scrapes the site [gogoanime](https://gogoanime.pe).

# For macs (complete these steps first)

Install homebrew first:

```
https://brew.sh/
```

then install 'util-linux' with homebrew:

```bash
brew install util-linux
```

next, run the following commands:

```bash
echo 'export PATH="/opt/homebrew/opt/util-linux/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/opt/homebrew/opt/util-linux/sbin:$PATH"' >> ~/.zshrc
export LDFLAGS="-L/opt/homebrew/opt/util-linux/lib"
export CPPFLAGS="-I/opt/homebrew/opt/util-linux/include"
export PKG_CONFIG_PATH="/opt/homebrew/opt/util-linux/lib/pkgconfig"
```

## Download

```bash
git clone https://github.com/joyryder/ani-cli.git
```

## Install

```bash
cd ani-cli
sudo make
```

## Usage

### watch anime

`ani-cli <query>`

### download anime

`ani-cli -d <query>`

### resume watching anime

`ani-cli -H`

### delete anime from history

`ani-cli -D`

### set video quality

`ani-cli -q 360`

By default `ani-cli` would try to get the best video quality available  
You can give specific qualities like `360/480/720/..`

You can also use special names:

- `best`: Select the best quality available
- `worst`: Select the worst quality available

Multiple episodes can be viewed/downloaded by giving the episode range like so

Choose episode [1-13]: 1 6

This would open/download episodes 1 2 3 4 5 6

## Dependencies

- grep
- curl
- sed
- mpv
- ffmpeg

## Misc

- Windows instructions can be found in this branch https://github.com/pystardust/ani-cli/tree/windows-vlc

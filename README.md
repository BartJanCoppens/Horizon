# Horizon

Horizon is an app for making presentations that you fly through instead of clicking through. Your slides stand in a 3D world, and you choose your route through them as you present. You can build a presentation yourself, or describe what you want and let an AI help you plan it and draw animated visuals for it.

It works on **Mac**, **Windows** and **Linux**. It's free and needs no account.

**[⬇ Download the latest version](https://github.com/BartJanCoppens/Horizon/releases/latest)**

---

## 1. Download

Open the [latest release](https://github.com/BartJanCoppens/Horizon/releases/latest), scroll down to **Assets** and click the file for your computer:

| Your computer | File to download |
|---|---|
| Mac with an Apple chip (M1, M2, M3, M4…) | `Horizon-<version>-arm64.dmg` |
| Mac with an Intel processor | `Horizon-<version>-x64.dmg` |
| Windows 10 or 11 | `Horizon-Setup-<version>-x64.exe` |
| Linux (most distributions) | `Horizon-<version>-x86_64.AppImage` |
| Linux (Ubuntu, Debian and similar, as a package) | `Horizon-<version>-amd64.deb` |

Not sure which Mac you have? Click the Apple menu  › **About This Mac**. If it says **Chip: Apple M…**, take the Apple chip file; if it says **Processor: Intel**, take the Intel file.

You can ignore the other files (`.zip`, `.blockmap`, `.yml`): the app uses them for its updates.

## 2. Install

Horizon is made by one person for friends and family, so it isn't registered with Apple or Microsoft. Your computer will therefore warn you the first time you open it. That's expected; the steps below show how to get past the warning once.

### Mac

1. Open the `.dmg` file you downloaded.
2. Drag **Horizon** onto the **Applications** folder in the window that appears.
3. Open **Horizon** from your Applications folder (or with Spotlight).
4. macOS says it can't check Horizon for malicious software and won't open it. Click **Done** (or **OK**).
5. Open **System Settings** › **Privacy & Security**, scroll down to the message about Horizon and click **Open Anyway**. Confirm with your password or Touch ID, then click **Open Anyway** once more.

From then on Horizon opens normally. Needs macOS 12 (Monterey) or later.

<details>
<summary>macOS says Horizon "is damaged and can't be opened"</summary>

This can happen with apps that aren't registered with Apple. Open the **Terminal** app, paste this line and press Return:

```sh
xattr -dr com.apple.quarantine /Applications/Horizon.app
```

Then open Horizon again.
</details>

### Windows

1. Double-click `Horizon-Setup-<version>-x64.exe`.
2. If Windows shows **Windows protected your PC**, click **More info**, then **Run anyway**.
3. Horizon installs by itself (no administrator rights needed) and opens. You'll find it in the Start menu afterwards.

Needs Windows 10 or 11, 64-bit.

### Linux

**AppImage** (works on most distributions):

```sh
chmod +x Horizon-*-x86_64.AppImage
./Horizon-*-x86_64.AppImage
```

Or right-click the file › **Properties** › **Permissions**, tick **Allow executing file as program**, then double-click it. On Ubuntu 22.04 or later, if it doesn't start, install FUSE first: `sudo apt install libfuse2` (on Ubuntu 24.04: `sudo apt install libfuse2t64`).

**Debian package:**

```sh
sudo apt install ./Horizon-*-amd64.deb
```

Horizon then appears in your applications menu.

## 3. Connect an AI (optional)

You can make presentations without any AI. To use the AI features (planning a presentation with you, drawing animated visuals, world events from a description), connect a model with your own key:

1. In Horizon, open **File › Models & keys…**
2. Choose a provider and paste your key. Your key is stored encrypted on your own computer and is only ever sent to that provider.

Where to get a key:

- **Claude** (recommended; Horizon is tuned for it): sign up at [console.anthropic.com](https://console.anthropic.com), add some credit under **Billing**, then create a key under **API keys**. You pay the provider for what you use.
- **OpenAI** or **Google Gemini**: create a key in their developer consoles ([platform.openai.com](https://platform.openai.com/api-keys), [aistudio.google.com](https://aistudio.google.com/apikey)).
- **Free and private, on your own computer**: install [Ollama](https://ollama.com) or [LM Studio](https://lmstudio.ai), download a model there, and pick it in **Models & keys…** (no key needed). Results are simpler than with Claude.

## Updates

- **Windows** and **Linux AppImage**: new versions download in the background and install the next time you restart Horizon.
- **Mac** and **Linux .deb**: Horizon tells you when a new version is ready, with a **Download** button. Install it the same way as the first time.

## Uninstall

- **Mac**: drag **Horizon** from Applications to the Bin.
- **Windows**: **Settings › Apps › Installed apps**, find Horizon › **Uninstall**.
- **Linux**: delete the AppImage, or run `sudo apt remove horizon-canvas`.

Your presentations are files you saved yourself (`.horizon`), so they stay where you put them.

## Questions or problems

Contact Bart Jan directly, or [open an issue](https://github.com/BartJanCoppens/Horizon/issues) here.

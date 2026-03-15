#  Shaggy Timer

**Live Event Timer & Display System**  
*by Video Maven Limited· [videomaven.co.uk](https://videomaven.co.uk)*

Shaggy Timer is a professional countdown timer and programme display system for live events. Run it on a backstage Mac or PC — speakers see a clean full-screen countdown on a tablet or monitor, and your operator controls everything from a browser-based control panel.

---

##  Downloads
To download, go to [Releases](https://github.com/VideoMaven/ShaggyTimer/releases)
| Platform | File | Notes |
|----------|------|-------|
| **Mac** (Apple Silicon) | `shaggytimer_mac_arm.zip` | M1/M2/M3/M4 Macs only |
| **Windows** | `Shaggy Timer Setup 1.0.0.exe` | Windows 10/11 x64 |
| **Bitfocus Companion Module** | `videomaven-shaggytimer-3.0.0.tgz` | Requires Companion 3.x |

---

##  Mac — Getting Started

1. Download `shaggytimer_mac_arm.zip` and unzip it
2. Double-click **Shaggy Timer.app** to launch
3. **First launch only:** macOS will block the app as it is unsigned. Right-click the app → **Open** → **Open** again in the dialog
4. The app opens automatically to the control panel
5. On the same network, open a browser on any tablet or monitor and go to the URL shown in the control panel (e.g. `http://192.168.1.x:3737/output`) for the speaker-facing display

---

##  Windows — Getting Started

1. Download `Shaggy Timer Setup 1.0.0.exe`
2. Run the installer — Windows may show a SmartScreen warning as the app is unsigned. Click **More info** → **Run anyway**
3. Shaggy Timer will install and launch automatically
4. The app opens to the control panel
5. On the same network, open a browser on any tablet or monitor and go to the URL shown in the control panel (e.g. `http://192.168.1.x:3737/output`) for the speaker-facing display

---

##  Using Shaggy Timer

### Setting Up Your Programme
- Click **+ Add Item** to add agenda items manually
- Or paste a URL in the **Import** box to auto-parse a schedule from a web page
- Each item has a title, speaker name, and duration
- Drag items to reorder

### Running the Event
| Action | How |
|--------|-----|
| Start a timer | Double-click an item, or single-click to select then hit **▶ Go** |
| Pause / Resume | **⏸ Pause** and **▶ Resume** buttons |
| Adjust time | **±30s** and **±1m** buttons |
| Mark complete | **✓ Done** — item greys out on both screens |
| Send a message | Type in the message box → **Send** — appears on the output screen |
| Clear message | **Stop** button next to the message box |

### Timer Colours (output screen)
| Colour | Meaning |
|--------|---------|
| 🟢 Green | More than 3 minutes remaining |
| 🟡 Yellow | 1–3 minutes remaining |
| 🔴 Red (pulsing) | Under 1 minute remaining |
| **+MM:SS** | Overrun — shows how long over |

### Accessing the Output Display
The output URL is shown in the bottom of the control panel. Open it on any device on the same Wi-Fi or network:
- `http://<your-ip>:3737/output`

You can also open it as a separate window from the **View** menu in the app.

---

## 🎛️ Bitfocus Companion Module

Control Shaggy Timer from a Stream Deck or any device supported by [Bitfocus Companion](https://bitfocus.io/companion).

### Installation

1. Download `videomaven-shaggytimer-3.0.0.tgz`
2. Open Bitfocus Companion in your browser
3. Go to **Manage Modules** (top right menu)
4. Click **Import module package**
5. Select the `.tgz` file
6. Go to **Connections** → click **+** → search for **Shaggy Timer**
7. Enter your Shaggy Timer machine's IP address and port `3737`
8. Click **Save** — the module will connect automatically

### Available Actions

| Action | Description |
|--------|-------------|
| Timer: Start Item | Start a specific item by number |
| Timer: Start Next | Start the next item in the list |
| Timer: Start Selected | Start whichever item is selected in the control panel |
| Timer: Pause | Pause the running timer |
| Timer: Resume | Resume a paused timer |
| Timer: Pause/Resume Toggle | Toggle between pause and resume |
| Timer: Stop | Stop the timer |
| Timer: Adjust | Add or subtract seconds from the running timer |
| Item: Mark Complete | Mark an item as done |
| Item: Mark Complete & Start Next | Mark done and immediately start next |
| Message: Set Text | Pre-fill the message box without sending live |
| Message: Send | Send a message to the output screen |
| Message: Stop | Clear the message from the output screen |

### Available Feedbacks

| Feedback | Description |
|----------|-------------|
| Timer Running | Button lights up when timer is active |
| Timer Paused | Button lights up when paused |
| Timer Overrun | Button lights up when over time |
| Timer Low | Button lights up when under a set threshold |
| Current Item Is | Button lights up when a specific item is active |
| Message Active | Button lights up when a message is live |

### Available Variables

| Variable | Description |
|----------|-------------|
| `$(shaggytimer:timer_remaining)` | Time remaining as MM:SS |
| `$(shaggytimer:timer_remaining_seconds)` | Time remaining in seconds |
| `$(shaggytimer:current_item_title)` | Title of the current item |
| `$(shaggytimer:current_item_speaker)` | Speaker of the current item |
| `$(shaggytimer:next_item_title)` | Title of the next item |
| `$(shaggytimer:next_item_speaker)` | Speaker of the next item |
| `$(shaggytimer:message_text)` | Current message text |

---

##  Network Setup Tips

- Shaggy Timer runs on port **3737**
- The control machine and output devices must be on the **same network**
- For reliable output displays at events, use a dedicated Wi-Fi access point or wired switch rather than the venue Wi-Fi
- The control panel shows all available IP addresses — use the one that matches your network

---

*Built with hope by SHAGGY

# F1 Race Replay 🏎️ 🏁

A Python application for visualizing Formula 1 race telemetry and replaying race events with interactive controls and a graphical interface.

![Race Replay Preview](./resources/preview.png)

## 🎯 What Is This?

F1 Race Replay transforms real Formula 1 telemetry data into an interactive race visualization. Think of it as your personal race director's screen - complete with live positions, tire strategies, and driver telemetry - but with magical powers to control time itself.

### Why This Exists

Because watching an F1 race once is never enough. Sometimes you need to:
- 🔍 **Analyze** - Where exactly did Leclerc lose those 3 tenths?
- 🎓 **Learn** - How do the best drivers take that corner?
- 🎮 **Enjoy** - Experience the race from a completely new perspective
- 📊 **Compare** - See two qualifying laps side-by-side with full telemetry

## ✨ Features

### 🎬 Time Control
- **Pause & Resume** - Freeze the action at any moment
- **Rewind** - Go back 5 seconds instantly
- **Fast Forward** - Skip the boring parts
- **Speed Control** - Watch at 0.5x, 1x, 2x, or 4x speed

### 📊 Live Data
- **Real-time Leaderboard** - See positions update as the race unfolds
- **Tire Compounds** - Visual indicators for SOFT/MEDIUM/HARD/WET
- **Driver Status** - Know who's racing, pitting, or out
- **Lap Counter** - Track progress through the race

### 🔬 Telemetry Insights
Click any driver to see:
- 🚀 **Speed** - Real-time km/h
- ⚙️ **Gear** - What gear they're in
- 🎯 **Throttle** - 0-100% application
- 💨 **DRS** - Open or closed
- 🏁 **Current Lap** - Track their progress

### 🏁 Qualifying Mode
- Compare up to 2 drivers side-by-side
- Overlay telemetry traces:
  - Speed through corners
  - Throttle application
  - Brake points
  - Gear changes
- Identify exactly where time is won and lost

## 🖼️ Gallery

```
┌─────────────────────────────────────────────────────────────┐
│  🏎️ F1 Race Replay - Monaco Grand Prix 2024                │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│         🏁 LAP 45/78          ⏱️ TIME: 01:23:45             │
│                                                              │
│    ┌──────────────────────────┐    ┌──────────────────┐    │
│    │   🗺️ TRACK MAP          │    │  📊 LEADERBOARD  │    │
│    │                          │    │                  │    │
│    │      ●  ←─────┐         │    │  1. VER 🔴  L45  │    │
│    │     ╱          │         │    │  2. HAM 🟡  L45  │    │
│    │    ╱           ↓         │    │  3. LEC 🔴  L45  │    │
│    │   ●            │         │    │  4. PER 🔴  L45  │    │
│    │    ╲          ╱          │    │  5. SAI 🔴  L45  │    │
│    │     ╲        ╱           │    │  ...             │    │
│    │      └──────●            │    │                  │    │
│    └──────────────────────────┘    └──────────────────┘    │
│                                                              │
│    ┌──────────────────────────────────────────────────┐    │
│    │  📈 TELEMETRY - VER                              │    │
│    │  Speed: 287 km/h  |  Gear: 7  |  DRS: OPEN      │    │
│    └──────────────────────────────────────────────────┘    │
│                                                              │
│         [⏸️ PAUSE]  [⏪ REW]  [⏩ FWD]  [⚡ 2.0x]          │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- 2GB free disk space (for cache)
- Decent internet connection (first run downloads telemetry)

### Installation

```bash
# Clone the repository
git clone https://github.com/Prajwal-koundinya/f1-visualization.git
cd f1-visualization

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Your First Replay

```bash
# List available races
python main.py --year 2024 --list-rounds

# Watch Monaco GP 2024
python main.py --year 2024 --round 8
```

**First run takes 5-10 minutes** (downloads telemetry). After that? Lightning fast! ⚡

## 🎮 Usage

### Race Replays

```bash
# Basic race replay
python main.py --year 2024 --round 12

# Sprint race
python main.py --year 2024 --round 11 --sprint

# Force refresh data
python main.py --year 2024 --round 8 --refresh-data
```

### Qualifying Sessions

```bash
# Regular qualifying
python main.py --year 2024 --round 8 --qualifying

# Sprint qualifying
python main.py --year 2024 --round 11 --qualifying --sprint
```

### Finding Races

```bash
# List all rounds
python main.py --year 2024 --list-rounds

# List only sprint weekends
python main.py --year 2024 --list-sprints
```

## ⌨️ Controls

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `SPACE` | Pause/Resume |
| `←` | Rewind 5 seconds |
| `→` | Fast forward 5 seconds |
| `↑` | Increase playback speed |
| `↓` | Decrease playback speed |
| `1` | Set speed to 0.5x |
| `2` | Set speed to 1.0x |
| `3` | Set speed to 2.0x |
| `4` | Set speed to 4.0x |

### Mouse Controls
- **Click driver** in leaderboard → View their telemetry
- **Click buttons** → Control playback
- **Click again** → Deselect driver

## 🎯 Use Cases

### 📚 For Learning
- Study racing lines through specific corners
- Understand tire strategy impacts
- See how top drivers manage DRS zones
- Compare braking points between drivers

### 🔬 For Analysis
- Identify where lap time is gained/lost
- Analyze overtaking opportunities
- Study stint management
- Compare qualifying performances

### 🎮 For Fun
- Relive epic battles in slow motion
- Watch an entire season's highlights
- Create your own race commentary
- Spot incidents you missed live

### 🏫 For Education
- Teaching tool for racing schools
- Understanding F1 strategy
- Data visualization demonstrations
- Sports analytics projects

## 🛠️ Tech Stack

- **[FastF1](https://github.com/theOehrly/Fast-F1)** - Official F1 telemetry data
- **[Arcade](https://api.arcade.academy/)** - High-performance graphics
- **NumPy & Pandas** - Data processing
- **Python 3.8+** - Core language
  

## File Structure

```
f1-race-replay/
├── main.py                    # Entry point, handles session loading and starts the replay
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
├── roadmap.md                 # Planned features and project vision
├── resources/
│   └── preview.png           # Race replay preview image
├── src/
│   ├── f1_data.py            # Telemetry loading, processing, and frame generation
│   ├── arcade_replay.py      # Visualization and UI logic
│   └── ui_components.py      # UI components like buttons and leaderboard
│   ├── interfaces/
│   │   └── qualifying.py     # Qualifying session interface and telemetry visualization
│   │   └── race_replay.py    # Race replay interface and telemetry visualization
│   └── lib/
│       └── tyres.py          # Type definitions for telemetry data structures
│       └── time.py           # Time formatting utilities
└── .fastf1-cache/            # FastF1 cache folder (created automatically upon first run)
└── computed_data/            # Computed telemetry data (created automatically upon first run)
```

## Customization

- Change track width, colors, and UI layout in `src/arcade_replay.py`.
- Adjust telemetry processing in `src/f1_data.py`.


# Known Issues

- The leaderboard appears to be inaccurate for the first few corners of the race. The leaderboard is also temporarily affected by a driver going in the pits. At the end of the race the leadeboard is sometimes affected by the drivers final x,y positions being further ahead than other drivers. These issues are known issues caused by innacuracies in the telemetry and being worked on for future releases. Its likely that these issues will be fixed in stages as improving the leaderboard accuracy is a complex task.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This is a fan-made educational project. Formula 1, F1, and related trademarks are property of Formula One Licensing BV. All data is sourced from publicly available APIs and used for educational and non-commercial purposes only.

## 🙏 Acknowledgments

- **[FastF1](https://github.com/theOehrly/Fast-F1)** - For making F1 data accessible
- **F1 Community** - For the passion that drives projects like this

## 📬 Contact

**Prajwal Koundinya**
- GitHub: [@Prajwal-koundinya](https://github.com/Prajwal-koundinya)
- Project Link: [f1-visualization](https://github.com/Prajwal-koundinya/f1-visualization)


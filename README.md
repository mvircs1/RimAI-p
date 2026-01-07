# RimAI - AI Storytelling for RimWorld

[![RimWorld Version](https://img.shields.io/badge/RimWorld-1.6+-blue.svg)](https://rimworldgame.com/)
[![.NET](https://img.shields.io/badge/.NET-4.7.2-green.svg)](https://dotnet.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Release](https://img.shields.io/github/v/release/Mvircs1/RimAI?include_prereleases)](https://github.com/Mvircs1/RimAI/releases)
[![GitHub Stars](https://img.shields.io/github/stars/Mvircs1/RimAI?style=social)](https://github.com/Mvircs1/RimAI/stargazers)

> Transform your RimWorld experience with an intelligent storyteller that creates dynamic, personalized events using artificial intelligence!

RimAI is a revolutionary mod that replaces RimWorld's traditional storyteller system with advanced AI capable of generating contextual narrative events based on your colony's current state. Featuring narrative arcs, dev mode chat, intelligent event generation, and a professional logging system for debugging!

## ✨ Features

### 🤖 Advanced AI
- **Contextual Events**: AI analyzes wealth, mood, population and colony situation to create relevant events
- **Intelligent Narrative**: Events tell a coherent story over time
- **Unique Personalities**: 4 distinct storyteller personalities (Balanced, Sadistic, Chaotic, Protective)

### 🎯 Event Types
- **Raids**: Enemy attacks adapted to colony strength
- **Diseases**: Realistic plagues and infections
- **Trade**: Caravans and orbital visits
- **Weather**: Extreme meteorological events
- **Animals**: Wild animal packs and manhunts
- **Visitors**: Diplomats and special visitors
- **Resources**: Resource drops and supply pods

### 🔧 Advanced Customization
- **Multiple Providers**: OpenRouter, OpenAI and Anthropic
- **Diverse Models**: From GPT-3.5 to Claude-3, choose your favorite
- **Frequency Control**: Adjust intervals between events
- **AI Influence**: Mix AI events with vanilla system
- **Smart Cache**: Cached responses for performance

### 🌍 Multilingual Support
- **Complete Portuguese**: Fully translated interface and events
- **English**: Full support for international players

### 🎭 Narrative Arcs (NEW!)
- **Long-term Storytelling**: AI creates cohesive story arcs spanning multiple events
- **4 Epic Arcs**: Pirate curses, mysterious plagues, cosmic storms, and merchant mysteries
- **Progressive Phases**: Introduction → Development → Climax → Resolution
- **Persistent Elements**: NPCs and locations that appear across events
- **Automatic Activation**: Arcs start organically based on colony state

### 🛠️ Dev Mode
- **AI Chat Commands**: Use "ai [message]" to request events in natural language
- **Event Commands**: Quick raid/trader/disease generation
- **Real-time Feedback**: Immediate AI responses with narrative context
- **Testing Tools**: Debug and test event generation

## 🚀 Quick Installation

### Prerequisites
- **RimWorld 1.6+**
- **Harmony Mod** (required)
- **API Key** (OpenRouter, OpenAI or Anthropic)

### Installation Steps

1. **Download the mod**
   - Download from [releases page](https://github.com/Mvircs1/RimAI/releases)
   - Or clone the repository for development

2. **Install in RimWorld**
   ```bash
   # Extract to RimWorld's Mods folder
   # Typical path: C:\Program Files (x86)\Steam\steamapps\common\RimWorld\Mods
   ```

3. **Configure the API**
   - Open RimWorld
   - Go to Mods → RimAI → Configure
   - Paste your API key
   - Choose your preferred AI model

4. **Select the Storyteller**
   - Start a new game
   - Choose "AI Oracle" as storyteller
   - Enjoy!

## 🔑 API Configuration

### Provider Options

| Provider | Free | Models | Cost | Notes |
|----------|------|--------|------|-------|
| **OpenRouter** | ✅ Free tier | 100+ models | Low | Recommended for beginners |
| **OpenAI** | ❌ | GPT-3.5/4 | Medium | Official OpenAI API |
| **Anthropic** | ❌ | Claude | High | Best reasoning capabilities |
| **Google Studio / Gemini** | ❌ | Gemini 1.5 | Medium | Google's multimodal model |
| **NanoGPT** | ✅ Free tier | NanoGPT | Low | Fast inference |
| **Groq** | ✅ Free tier | Mixtral, Llama | Low | Ultra-fast inference |
| **OpenAI Compatible** | Varies | Any compatible | Varies | Custom API endpoints |

### Getting API Keys

#### OpenRouter (Recommended for Beginners)
1. Visit [openrouter.ai/keys](https://openrouter.ai/keys)
2. Create a free account
3. Generate your API key
4. **Bonus**: $5 free credits!

#### OpenAI
1. Visit [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
2. Login/create account
3. Navigate to API Keys
4. Create a new key

#### Anthropic
1. Visit [console.anthropic.com](https://console.anthropic.com/)
2. Sign up
3. Go to API Keys
4. Generate your key

#### Google Studio / Gemini
1. Visit [makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey)
2. Create a Google Cloud account
3. Enable AI Studio API
4. Generate your API key

#### NanoGPT
1. Visit [nano-gpt.com](https://nano-gpt.com/)
2. Create a free account
3. Get your API key from dashboard

#### Groq
1. Visit [console.groq.com/keys](https://console.groq.com/keys)
2. Create a free account
3. Generate your API key

#### OpenAI Compatible
- Configure your custom API endpoint URL in the mod settings
- Ensure the API follows OpenAI's chat completion format
- Check documentation for specific authentication requirements

## 🛠️ Development

### Environment Setup

#### Development Prerequisites
- **RimWorld 1.6.x** installed
- **.NET Framework 4.7.2 SDK**
- **Visual Studio 2022** or **VS Code** with C# extension
- **Harmony Mod** installed in RimWorld

#### Project Configuration

1. **Clone the repository**
   ```bash
   git clone https://github.com/Mvircs1/RimAI.git
   cd RimAI
   ```

2. **Configure RimWorld paths**
   ```bash
   cd Source/RimAI
   copy RimWorldPaths.props.example RimWorldPaths.props
   ```

   Edit `RimWorldPaths.props`:
   ```xml
   <RimWorldPath>C:\Program Files (x86)\Steam\steamapps\common\RimWorld</RimWorldPath>
   <HarmonyPath>C:\Program Files (x86)\Steam\steamapps\common\RimWorld\Mods\Harmony\Current\Assemblies</HarmonyPath>
   ```

3. **Build the project**
   ```bash
   dotnet build --configuration Release
   ```

### Project Structure

```
RimAI/
├── 1.6/                          # RimWorld mod files
│   ├── Assemblies/               # Compiled DLLs
│   │   └── RimAI.dll            # Main assembly
│   ├── Defs/                     # XML definitions
│   │   └── StorytellerDefs/     # Storyteller definitions
│   ├── Languages/                # Translations
│   │   ├── English/             # English
│   │   └── Portuguese/          # Brazilian Portuguese
│   └── Textures/                 # UI textures
├── Source/RimAI/                 # C# source code
│   ├── API/                      # API communication
│   │   ├── OpenRouterClient.cs  # HTTP client for APIs
│   │   ├── PromptBuilder.cs     # Prompt builder
│   │   ├── ResponseParser.cs    # JSON response parser
│   │   └── RateLimiter.cs       # Rate limiting
│   ├── Core/                     # Main logic
│   │   ├── RimAI_Mod.cs         # Main mod class
│   │   ├── RimAI_GameComponent.cs # Persistent game state
│   │   └── RimAI_WorldComponent.cs # World state
│   ├── Storytelling/             # Narrative system
│   │   ├── AIStorytellerComp.cs # AI storyteller component
│   │   ├── NarrativeContext.cs  # Narrative context
│   │   └── StorytellerDef_AI.cs # AI storyteller definitions
│   ├── UI/                       # User interface
│   │   ├── RimAI_SettingsWindow.cs # Settings window
│   │   ├── APIKeyDialog.cs      # API key dialog
│   │   └── NarrativeLogWindow.cs # Narrative log window
│   └── Utils/                    # Utilities
│       ├── CacheManager.cs      # Cache management
│       ├── GameStateSerializer.cs # Game state serialization
│       └── Logger.cs            # Logging system
├── About/                        # Mod metadata
│   ├── About.xml                # Mod information
│   ├── Preview.png              # Preview image
│   └── PublishedFileId.txt      # Steam Workshop ID
└── README.md                     # This file
```

## 🎮 How to Use

### Basic Settings
1. **API Provider**: Choose between OpenRouter (recommended), OpenAI or Anthropic
2. **Model**: Select the AI model (e.g.: `openai/gpt-3.5-turbo` for low cost)
3. **Personality**: Balanced for fair gameplay, Sadistic for extreme challenge
4. **Language**: Portuguese or English

### Advanced Settings
- **AI Influence**: 100% = AI only, 0% = vanilla only
- **Frequency**: Interval between events (0.5-3 days recommended)
- **Cache**: Keeps similar responses cached
- **Debug**: Enable for detailed logs

### Advanced Features

#### 🤖 AI Creativity Control
Control how "creative" or predictable the AI storyteller is:

- **Manual Control**: Set creativity level from 0.3 (Conservative) to 1.0 (Chaotic)
- **Dynamic Mode**: Let the AI automatically adjust creativity based on personality:
  - **Sadistic/Protective**: 0.4-0.5 (Focused & Strategic)
  - **Balanced**: 0.7 (Balanced Creativity)
  - **Chaotic**: 0.8-0.9 (Wild & Unpredictable)

#### 📊 Suffering Metrics (Inspired by Rimteller)
The AI now considers colony hardship when choosing events:
- **Downed colonists**: Currently incapacitated pawns
- **Damage taken**: Recent injuries and their severity
- **Death estimates**: Recent colony losses
- **Suffering levels**: From "None" to "Extreme crisis"

#### 🕰️ Narrative Pressure (Boredom Counters)
The AI tracks "narrative pressure" to prevent repetitive storytelling:
- **Days since last raid**: Creates pressure for combat events
- **Days since last trade**: Builds anticipation for economic events
- **Days since last disease**: Allows for health-related tension
- **Days since last weather**: Enables environmental storytelling
- **Days without visitors**: Creates social narrative opportunities
- **Overall variety**: Ensures diverse event types over time

**Example**: If it's been 45 days since the last raid, the AI feels narrative pressure to "break the peace" even with good colony morale.

### Usage Tips
- **Start small**: Use free OpenRouter to test
- **Monitor costs**: Track API usage on provider dashboard
- **Adjust difficulty**: Modify personality based on your experience
- **Backup frequently**: AI events can be unpredictable!
- **Fine-tune creativity**: Use dynamic mode for authentic personalities, manual for precise control

## ❓ FAQ

### General
**Q: Is the mod compatible with other mods?**
A: Yes, but some storyteller mods may conflict. Disable other storytellers when using RimAI.

**Q: Does it work in multiplayer?**
A: No, the mod is designed for single-player only.

**Q: How much does it cost to use?**
A: Depends on the provider. OpenRouter has a free tier. OpenAI ~$0.002/1k tokens.

### Technical
**Q: Events are not being generated**
A: Check if the API key is correct and if there's internet connection.

**Q: Game becomes slow**
A: Decrease event frequency or increase cache.

**Q: Compilation error**
A: Make sure RimWorld paths are correct in RimWorldPaths.props.

### Gameplay
**Q: Events are too difficult/easy**
A: Adjust the storyteller personality or AI influence.

**Q: How to disable temporarily**
A: Set AI influence to 0% in settings.

## 🔧 Troubleshooting

### Common Issues

#### ❌ "Invalid API Key"
```
Check if the key was copied correctly
OpenRouter keys start with "sk-or-v1-"
OpenAI keys start with "sk-"
Anthropic keys start with "sk-ant-"
```

#### ❌ "Could not find assembly"
```
Check if RimWorldPaths.props is configured
Make sure RimWorld and Harmony are installed
Rebuild project after changes
```

#### ❌ No events being generated
```
✓ Check internet connection
✓ Confirm API key is valid
✓ Enable debug mode for logs
✓ Verify storyteller is selected
```

#### ❌ Events failing
```
Debug mode shows "CanFireNow = false"
This means the event cannot occur at the current time
It's normal - AI will try again next cycle
```

### Debug Logs
To diagnose problems:
1. Enable "Debug Mode" in settings
2. Open game console (~)
3. Look for `[RimAI]` messages
4. Copy relevant logs to GitHub issues

### Performance
- **CPU**: Minimal usage during normal gameplay
- **Memory**: ~50MB additional for cache
- **Network**: API calls only when necessary
- **Storage**: Logs and cache (cleaned automatically)

## 🤝 Contributing

### How to Contribute
1. **Fork** the project
2. **Clone** your fork: `git clone https://github.com/Mvircs1/RimAI.git`
3. **Create a branch**: `git checkout -b feature/new-feature`
4. **Configure** RimWorld paths
5. **Develop** your feature
6. **Test** compilation: `dotnet build --configuration Release`
7. **Test in game** with different scenarios
8. **Commit**: `git commit -m "Add new feature"`
9. **Push**: `git push origin feature/new-feature`
10. **Pull Request** with detailed description

### Guidelines
- **Code**: Follow C# and RimWorld standards
- **Commits**: Clear messages in Portuguese/English
- **Testing**: Test with different configurations
- **Documentation**: Update README for new features
- **Issues**: Use templates for bugs and features

### Contribution Types
- 🐛 **Bug fixes**: Bug corrections
- ✨ **Features**: New functionalities
- 📚 **Documentation**: README/docs improvements
- 🎨 **UI/UX**: Interface improvements
- 🌍 **Translation**: Support for new languages
- ⚡ **Performance**: Optimizations

## 🗺️ Roadmap

### Upcoming Features
- [ ] **Custom events** created by players
- [ ] **Integration with popular mods** (DLCs, expansions)
- [ ] **Multiple simultaneous arcs** for complex narratives
- [ ] **Replay analysis** to learn player patterns
- [ ] **Offline mode** with local models
- [ ] **REST API** for external tool integration

### ✅ Recently Implemented
- [x] **Advanced narrative system** with story arcs (v1.0)
- [x] **Dev mode chat** with AI commands
- [x] **MIT License** and professional documentation

### Planned Improvements
- [ ] Polished interface
- [ ] More customization options
- [ ] Support for multiple simultaneous personalities
- [ ] Player feedback system
- [ ] Event statistics analysis

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### Credits
- **Harmony**: For RimWorld patching
- **Newtonsoft.Json**: For JSON parsing
- **OpenRouter**: AI models platform
- **RimWorld Community**: Inspiration and support

---

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/Mvircs1/RimAI/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Mvircs1/RimAI/discussions)
- **Discord**: [RimWorld Community Server](https://discord.gg/rimworld)
- **Reddit**: [r/RimWorld](https://reddit.com/r/rimworld)

---

**Made with ❤️ for the RimWorld community**

*Transform your colony into an epic story with AI!*

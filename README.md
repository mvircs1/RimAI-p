# RimAI - AI Storytelling for RimWorld

RimAI is a mod for RimWorld that replaces the traditional storyteller system with advanced AI capable of generating contextual narrative events based on your colony's current state.

## Key Features

- **Contextual Events**: AI analyzes wealth, mood, population and colony situation to create relevant events
- **Intelligent Narrative**: Events tell a coherent story over time
- **Unique Personalities**: 4 distinct storyteller personalities (Balanced, Sadistic, Chaotic, Protective)
- **Narrative Arcs**: Creates epic stories in progressive phases
- **Multilingual Support**: Complete interface in English and Portuguese

## Event Types

- Raids adapted to colony strength
- Realistic diseases
- Caravans and orbital visits
- Extreme weather events
- Wild animal attacks
- Diplomatic visitors
- Resource drops

## Installation

### Prerequisites
- RimWorld 1.6 or higher
- Harmony mod (required)
- API Key (OpenRouter, OpenAI or Anthropic)

### Installation Steps

1. Download the mod and extract to RimWorld's Mods folder
   - Typical path: `C:\Program Files (x86)\Steam\steamapps\common\RimWorld\Mods`

2. Open RimWorld
3. Go to Mods → RimAI → Configure
4. Paste your API key
5. Choose the preferred AI model

6. Start a new game
7. Select "AI Oracle" as storyteller

## API Configuration

### Provider Options

| Provider | Free | Models | Cost |
|----------|------|--------|------|
| OpenRouter | ✅ Free tier | 100+ models | Low |
| OpenAI | ❌ | GPT-3.5/4 | Medium |
| Anthropic | ❌ | Claude | High |

### Getting API Keys

#### OpenRouter (Recommended)
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

## Usage

### Basic Settings
- **API Provider**: Choose between OpenRouter (recommended), OpenAI or Anthropic
- **Model**: Select the AI model (e.g.: `openai/gpt-3.5-turbo` for low cost)
- **Personality**: Balanced for fair gameplay, Sadistic for extreme challenge
- **Language**: Portuguese or English

### Advanced Settings
- **AI Influence**: 100% = AI only, 0% = vanilla only
- **Frequency**: Interval between events (0.5-3 days recommended)
- **Cache**: Keeps similar responses cached
- **Debug**: Enable for detailed logs

### Usage Tips
- Start small using the free OpenRouter to test
- Monitor costs on the provider dashboard
- Adjust difficulty by modifying the personality
- Backup frequently - AI events can be unpredictable!

## Dev Mode
- Use "ai [message]" commands in console (~) to request events in natural language
- Quick commands to generate raid/trader/disease
- Real-time feedback with narrative context

## Support

- Verify the API key is correct
- Confirm internet connection
- Enable debug mode for logs
- Open the game console (~) and look for `[RimAI]` messages

## Compatibility

- Compatible with other mods, but may conflict with storyteller mods
- Disable other storytellers when using RimAI
- Designed for single-player only

---

**Transform your colony into an epic story with AI!**

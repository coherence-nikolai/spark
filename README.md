# 🧭 Coherence Compass - Navigate Your Mental Wellness Journey

*Find your inner coherence through AI-powered insights and personalized guidance*

## 🧭 What Makes This Revolutionary?

This isn’t just another mental health tracker. Coherence Compass is a **complete paradigm shift** in digital wellness tools - helping you navigate toward inner coherence through intelligent tracking and AI-powered insights.

### 🤖 **AI-Powered Insights** (Ready for Claude API Integration)

- Personalized coaching based on your unique patterns
- Context-aware suggestions and interventions
- Pattern detection that goes beyond simple correlations
- **Note:** Requires Anthropic API key for full AI features

### 🎨 **Stunning Organic Design**

- Warm, earthy color palette (terracotta, sage, warm beige) - like a compass rose
- Beautiful Crimson Pro serif + Albert Sans typography
- Breathing animations that guide you like a steady compass
- Smooth, natural micro-interactions
- Full dark mode with warm, grounding tones

### ✨ **Revolutionary Features**

Your compass to mental wellness:

1. **Voice Journaling** - Speak your thoughts naturally using Web Speech API
1. **Guided Breathing** - Animated 4-4-4 breathing exercise with visual guidance
1. **Advanced Pattern Detection** - Discovers correlations between factors and mood
1. **Streak Tracking** - Gamified consistency to build habits
1. **Smart Insights** - AI identifies your best days, optimal routines
1. **Goal Tracking** - Set and achieve wellness goals
1. **Crisis Resources** - Instant access to mental health support
1. **Export Everything** - Own your data completely
1. **PWA Ready** - Install as native app on any device
1. **100% Private** - Zero server communication, all local storage

## 📊 Key Improvements Over V1

|Feature            |V1                     |V2                       |
|-------------------|-----------------------|-------------------------|
|Design             |Generic purple gradient|Warm organic minimalism  |
|Typography         |System fonts           |Crimson Pro + Albert Sans|
|AI Coaching        |❌                      |✅ (API ready)            |
|Voice Input        |❌                      |✅                        |
|Breathing Exercises|❌                      |✅ Animated               |
|Pattern Detection  |Basic                  |Advanced ML-style        |
|Streak Tracking    |❌                      |✅                        |
|Best Day Analysis  |❌                      |✅                        |
|Dark Mode          |❌                      |✅ Warm theme             |
|Crisis Resources   |❌                      |✅ Built-in               |
|Animations         |Minimal                |Organic, breathing       |

## 🎯 Quick Start

### Option 1: Use Immediately

1. Download `index.html`
1. Open in any modern browser
1. Start your wellness journey!

### Option 2: GitHub Pages

```bash
# Fork this repo, then:
git clone your-fork-url
cd coherence-compass
# Enable GitHub Pages in repo settings
# Your app will be live at yourusername.github.io/coherence-compass
```

### Option 3: Deploy Anywhere

Works on:

- Netlify (drag & drop)
- Vercel
- Cloudflare Pages
- Any static host

## 🤖 Enabling AI Coach

To activate the AI coaching feature:

1. Get an Anthropic API key from https://console.anthropic.com/
1. Open `index.html` in a text editor
1. Find the `getAIResponse()` function (around line 800)
1. Replace the placeholder with actual API calls:

```javascript
async function getAIResponse(userMessage, context) {
    const response = await fetch("https://api.anthropic.com/v1/messages", {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
            "x-api-key": "YOUR_API_KEY_HERE",  // Add your key
            "anthropic-version": "2023-06-01"
        },
        body: JSON.stringify({
            model: "claude-sonnet-4-20250514",
            max_tokens: 1000,
            messages: [{
                role: "user",
                content: `Context: ${context}
User question: ${userMessage}
Please provide supportive, evidence-based mental health guidance.`
            }]
        })
    });

    const data = await response.json();
    return data.content[0].text;
}
```

## 💡 Advanced Features Guide

### Voice Journaling

- Click the 🎤 button while journaling
- Speak naturally for up to 30 seconds
- Text appears automatically
- **Requires:** Chrome/Edge (uses Web Speech API)

### Breathing Exercise

- Navigate to the Breathe tab
- Click “Start” to begin 4-4-4 breathing
- Follow the animated circle:
  - Expands = Inhale (4s)
  - Holds = Hold breath (4s)
  - Contracts = Exhale (4s)
  - Pause = Rest (2s)
- Practice daily for anxiety reduction

### Pattern Detection

After 3+ check-ins, insights automatically appear:

- **Exercise Correlation** - Impact of physical activity on mood
- **Sleep Quality** - How rest affects energy levels
- **Social Connection** - Benefits of human interaction
- **Stress Patterns** - Work stress impact analysis
- **Meditation Effects** - Mindfulness practice results

### Goal System

1. Set SMART goals (“Meditate 10min daily”)
1. Check off as completed
1. Track progress over time
1. Build sustainable habits

## 🎨 Customization Guide

### Changing Colors

Edit CSS variables in `<style>`:

```css
:root {
    --primary: #D4773C;      /* Main terracotta */
    --secondary: #7A9D7E;    /* Sage green */
    --accent: #E8B86D;       /* Warm gold */
    /* Change these to your preferred palette */
}
```

### Adding New Factors

Find the tag section (~line 250 in HTML):

```html
<button type="button" class="tag" data-tag="your_factor">🎵 Music</button>
```

### Customizing Insights

Edit `detectPatterns()` function to add your own correlation algorithms.

## 📱 Mobile Installation

### iOS (Safari)

1. Open the app in Safari
1. Tap Share button
1. Select “Add to Home Screen”
1. Icon appears on home screen

### Android (Chrome)

1. Open in Chrome
1. Tap three dots menu
1. Select “Install app” or “Add to Home screen”

## 🔒 Privacy & Data

### What’s Stored Locally:

- All check-in entries
- Goal list
- Theme preference
- Chat history (if using AI coach)

### What’s NEVER Sent:

- Your personal data
- Check-in details
- Journal entries
- Any analytics or tracking

### Data Export:

- Click “Export All Data” in About tab
- Downloads JSON file with everything
- Import to other tools or backup
- Delete from app anytime

## 🆘 Crisis Resources

Built-in quick access to:

- National Suicide Prevention Lifeline: **988**
- Crisis Text Line: Text **HELLO** to **741741**
- International resources
- **Note:** App is a wellness tool, not emergency service

## 🛠️ Technical Stack

- **Frontend:** Pure HTML/CSS/JavaScript (no frameworks!)
- **Charts:** Chart.js for visualizations
- **Fonts:** Google Fonts (Crimson Pro + Albert Sans)
- **Storage:** LocalStorage API
- **Voice:** Web Speech API
- **PWA:** Service Worker ready (add manifest.json)
- **AI:** Anthropic Claude API (optional integration)

## 🌟 Best Practices

### For Consistency:

- Check in same time daily (morning or evening)
- Use voice notes when you don’t feel like typing
- Review insights weekly
- Set 1-2 realistic goals to start

### For Insights:

- Track for at least 2-3 weeks before drawing conclusions
- Be honest in check-ins
- Note context in journal entries
- Look for patterns, not perfection

### For Mental Health:

- App complements, doesn’t replace therapy
- Use breathing exercises during stress
- Contact crisis resources if needed
- Celebrate small wins and progress

## 🚧 Roadmap (Future Enhancements)

Planned features:

- [ ] Mood prediction ML model
- [ ] Photo mood board
- [ ] Habit correlation matrix
- [ ] Weekly email summaries
- [ ] Community insights (anonymized)
- [ ] Therapist sharing mode
- [ ] Apple Health / Google Fit integration
- [ ] Guided CBT exercises
- [ ] Gratitude prompts
- [ ] Weather correlation

## 🤝 Contributing

Want to make it even better?

1. Fork the repo
1. Create a feature branch
1. Make your improvements
1. Test thoroughly
1. Submit a pull request

Ideas welcome:

- New insight algorithms
- Additional visualizations
- More breathing techniques
- UI/UX improvements
- Accessibility enhancements

## 📄 License

MIT License - Use freely, modify, distribute!

## 💝 Support

Love the app? Here’s how to help:

- ⭐ Star the repo
- 🐛 Report bugs via GitHub Issues
- 💡 Suggest features
- 📢 Share with others who might benefit
- 🔧 Contribute code improvements

## ⚠️ Important Disclaimers

1. **Not Medical Advice:** This app is for general wellness tracking, not diagnosis or treatment
1. **See Professionals:** If experiencing severe mental health issues, consult licensed providers
1. **Emergency Services:** For crisis situations, call emergency services (911 in US) or crisis hotlines
1. **AI Limitations:** AI coach provides general guidance, not personalized medical advice
1. **Beta Software:** While tested, use at your own discretion

## 🎓 Evidence-Based Features

Our features are grounded in research:

- **Mood Tracking:** Shown to improve self-awareness (Kauer et al., 2012)
- **Breathing Exercises:** Reduces anxiety (Jerath et al., 2015)
- **Pattern Recognition:** Helps identify triggers (Schueller & Parks, 2014)
- **Goal Setting:** Increases achievement likelihood (Locke & Latham, 2002)
- **Journaling:** Improves mental health outcomes (Pennebaker, 1997)

## 📬 Contact

Questions? Feedback? Reach out:

- GitHub Issues for bugs
- Discussions for feature requests
- Email for sensitive topics

-----

**Remember:** You’re not alone. Mental health matters. Let Coherence Compass guide you on your wellness journey, one day at a time. 🧭💚

*Navigate toward inner coherence. Chart your path to wellness.*

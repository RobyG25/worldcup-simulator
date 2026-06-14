# ⚽ 2026 FIFA World Cup Match Simulator

A powerful client-side web application that runs **100 Monte Carlo simulations** for every 2026 FIFA World Cup match to predict scores, winners, and betting odds.

## 🌟 Features

✅ **100 Match Simulations Per Game** - Uses weighted randomization for realistic outcomes  
✅ **Hybrid Prediction Model** - Combines:
   - Team Rating/Strength
   - Goals Per Game Average
   - Recent Form
   - Defensive Strength
   - Home Field Advantage

✅ **Comprehensive Tournament Coverage** - Group stage through finals  
✅ **Pre-Match Statistics** - Team ratings, goals per game, form metrics  
✅ **Multiple Score Predictions** - Average, Median, and Most Likely scores  
✅ **Decimal Betting Odds** - Dynamically calculated from simulation probabilities  
✅ **Confidence Indicators** - Shows prediction certainty levels  
✅ **One-Page Display** - All 27+ matches visible with minimal scrolling  
✅ **100% Client-Side** - No server required, GitHub Pages compatible  
✅ **Minimal Clean Design** - Data-focused, professional interface  

## 📊 Prediction Algorithm

Each match is simulated 100 times using:

```
Expected Goals = Base Goals × Form Factor × Defensive Multiplier × Home Advantage
```

**Factors:**
- **Team Rating**: ELO-style rating (1400-1650)
- **Goals Per Game**: Historical scoring rate (1.2-1.9)
- **Form**: Recent performance multiplier (0.9-1.15)
- **Defensive Strength**: Opponent vulnerability factor (0.70-0.90)
- **Home Advantage**: 15% boost for home team

The simulator then randomizes around expected values to generate realistic score distributions.

## 🚀 Quick Start

### Option 1: GitHub Pages Deployment (Recommended)

1. **Fork this repository** or download the files
2. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Select main branch, / (root) folder
   - Save

3. **Access your simulator:**
   ```
   https://yourusername.github.io/worldcup-simulator/
   ```

### Option 2: Local Usage

1. **Download `worldcup_simulator.html`**
2. **Open in your web browser:**
   ```bash
   open worldcup_simulator.html
   # or
   firefox worldcup_simulator.html
   ```

### Option 3: Run with Python Server

```bash
# Python 3
python -m http.server 8000

# Then visit: http://localhost:8000
```

## 📁 Project Structure

```
worldcup-simulator/
├── worldcup_simulator.html    # Main application (all-in-one)
├── README.md                   # This file
└── assets/                     # (Optional) For future enhancements
    ├── css/
    ├── js/
    └── data/
```

## 💻 How to Use

1. **Open the application** in your browser
2. **Click "Run 100 Simulations"** button
3. **Wait for the magic** ✨ (usually 2-3 seconds)
4. **Scroll through results** to see:
   - Match details & tournament stage
   - Pre-match team statistics
   - Predicted scores (avg, median, most likely)
   - Predicted winner with win probability
   - Betting odds in decimal format
   - Confidence level of prediction

## 📈 Results Breakdown

**For each match you'll see:**

| Column | Details |
|--------|---------|
| Stage | Tournament phase (Group A, Quarterfinals, etc) |
| Match | Home vs Away team |
| Pre-Match Stats | Ratings, goals/game, form |
| Predicted Score | Average, Median, Most Common |
| Winner | Most likely outcome with probability |
| Odds (Decimal) | Win/Draw/Loss odds derived from simulation |
| Confidence | Prediction certainty (Very High to Very Low) |

## 🎯 Data Sources

**Team Statistics:**
- FIFA Rankings (as of 2024)
- Offensive & Defensive Strength
- Recent Form Metrics
- Historical Goals Per Game

**Matches:**
- All 64 confirmed 2026 World Cup matches
- Includes: Group Stage, Round of 16, Quarters, Semis, Final

## 🔧 Customization

### Add More Teams
Edit the `DEFAULT_TEAM_STATS` object:
```javascript
'Your Team': { 
    rating: 1500, 
    goalsPerGame: 1.6, 
    form: 1.05, 
    defensiveStrength: 0.85 
}
```

### Adjust Simulation Parameters
Modify in the `MatchSimulator` class:
- Change home advantage multiplier (currently 1.15)
- Adjust defensive impact (currently 0.2)
- Modify goal calculation formula

### Add More Matches
Update the `FALLBACK_MATCHES` array with additional fixtures

## 🎨 Styling

The app uses:
- **Color Scheme**: Purple gradient (#667eea to #764ba2)
- **Typography**: Segoe UI, clean and minimal
- **Responsive Design**: Works on desktop, tablet, mobile
- **Accessible**: High contrast, readable fonts

Customize colors by modifying the CSS variables in `<style>` section.

## 📱 Browser Compatibility

✅ Chrome/Chromium 90+  
✅ Firefox 88+  
✅ Safari 14+  
✅ Edge 90+  
✅ Mobile Browsers (iOS Safari, Chrome Mobile)

## ⚙️ Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Architecture**: Single-page application (SPA)
- **Simulation**: Monte Carlo method with weighted probability
- **Data Format**: JSON (embedded in HTML)
- **Deployment**: Static hosting (GitHub Pages, Netlify, Vercel, etc.)

## 📊 Interpretation Guide

**Confidence Levels:**
- 🔥 **Very High (70%+)**: Strong prediction, high probability winner
- 📈 **High (55-70%)**: Likely outcome, favored result
- ⚖️ **Moderate (45-55%)**: Could go either way, relatively balanced
- 📉 **Low (30-45%)**: Underdog prediction
- ❓ **Very Low (<30%)**: Long shot, unlikely outcome

**Betting Odds:**
- Numbers derived from simulation win probabilities
- Decimal format (European standard)
- Example: 2.50 means you win 2.50x your bet if successful

## 🐛 Troubleshooting

**Issue: Simulations don't run?**
- Clear browser cache (Ctrl+Shift+Del)
- Try in incognito/private mode
- Check browser console for errors (F12)

**Issue: Matches not showing?**
- Refresh the page
- Check JavaScript is enabled
- Try a different browser

**Issue: Odds look wrong?**
- This is normal - they're calculated from probabilities
- Higher probability = lower odds (better for home team)

## 🚀 Future Enhancements

- [ ] Real-time API integration for live odds
- [ ] Player injury impact on predictions
- [ ] Weather condition factors
- [ ] Team head-to-head history analysis
- [ ] Export results to CSV/PDF
- [ ] Historical accuracy tracking
- [ ] Interactive team comparison tool
- [ ] Custom simulation parameters UI

## 📜 License

This project is open source and available under the MIT License. Feel free to fork, modify, and deploy!

## 🤝 Contributing

Found a bug or have an idea? 
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

For issues, questions, or suggestions:
- Open a GitHub Issue
- Check existing issues for solutions
- Include browser type and any error messages

## ⭐ Enjoy!

Run simulations, analyze predictions, and enjoy the beautiful game! ⚽

---

**Last Updated:** 2026  
**Tournament:** FIFA World Cup 2026  
**Matches:** 64  
**Simulations per Match:** 100  
**Total Simulations:** 6,400+

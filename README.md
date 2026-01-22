# Spell Warrior - English Learning Game

An interactive, gamified English spelling game where players defeat monsters by spelling words correctly!

## Features

### 🎮 Gameplay
- **Monster Combat**: Defeat monsters by spelling English words correctly
- **Progressive Difficulty**: Three increasing levels with harder vocabulary
- **Combo System**: Build combo multipliers for consecutive correct answers
- **Damage System**: Correct spellings deal damage; longer combos = more damage
- **Multiple Monsters**: Defeat 3 monsters per level to advance

### 📚 Learning Features
- **Word Definitions**: Clear definitions for context
- **Parts of Speech**: Learn proper word classification
- **Pronunciation**: Click "Pronounce" to hear words (requires Web Speech API support)
- **Hints**: Get partial letter reveals to guide spelling
- **Progress Tracking**: Save your stats and track improvement

### 📊 Statistics
- Words learned count
- Accuracy percentage
- Monsters defeated tracker
- Highest level reached
- Persistent storage (localStorage)

## How to Play

1. **Start the Game**: Click "Start Game" from the main menu
2. **Read the Definition**: Learn what the word means
3. **Listen/Observe**: Click "Pronounce" to hear the word
4. **Type the Spelling**: Enter the correct spelling in the input field
5. **Check Your Answer**: Press Enter or click "Check"
6. **Build Combos**: Get consecutive words right to boost damage
7. **Defeat Monsters**: Each correct answer damages the current monster
8. **Level Up**: Defeat all 3 monsters in a level to advance

## Controls

- **Type**: Enter your spelling attempt
- **Enter Key**: Submit your answer
- **🔊 Pronounce**: Hear the word pronunciation
- **💡 Hint**: Get a hint (shows first half of letters)
- **✓ Check**: Submit your spelling
- **Pause**: Pause the game
- **Quit**: Return to main menu

## Levels

### Level 1 - Beginner
Common English words perfect for beginners:
- beautiful, celebrate, necessary, question, separate

### Level 2 - Intermediate
Trickier spellings with common mistakes:
- accommodate, privilege, embarrass, rhythm, receive, maintenance

### Level 3 - Advanced
Challenging words for advanced learners:
- bureaucracy, surveillance, parallel, miscellaneous, deliberately, anonymous

## Game Mechanics

### Health System
- Monster starts with 100 HP
- Each incorrect answer gives you another chance
- Each correct answer deals 20-50+ damage (depending on combo)

### Scoring
- Base: +10 points per correct word
- Combo Bonus: +5 points per combo level
- Formula: 10 + (combo × 5) points

### Combo System
- Resets to 0 on incorrect answers
- Increases with each correct answer
- Increases damage dealt to monsters
- Multiplies your score

## Statistics & Storage

Your statistics are automatically saved to your browser's local storage:
- Words Learned
- Total Correct Spellings
- Accuracy Percentage
- Monsters Defeated
- Highest Level Reached

You can reset statistics anytime from the Stats menu.

## Technical Details

### Technologies Used
- **HTML5**: Semantic structure
- **CSS3**: Responsive design, animations, gradients
- **JavaScript (ES6+)**: Game logic, state management
- **Web Speech API**: Pronunciation feature
- **LocalStorage**: Data persistence

### Browser Support
- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support (limited pronunciation on some versions)
- Mobile: Responsive design (optimized for tablets and phones)

### File Structure
```
├── index.html      # Game HTML structure
├── styles.css      # Responsive styling and animations
├── script.js       # Game logic and mechanics
└── README.md       # This file
```

## Customization

### Adding New Words
Edit the `wordDatabase` in `script.js`:

```javascript
const wordDatabase = {
    level1: [
        {
            word: "your-word",
            definition: "Word definition here",
            partOfSpeech: "part-of-speech"
        },
        // Add more words...
    ],
    // Add more levels...
};
```

### Adjusting Difficulty
Modify these values in `script.js`:
- Monster HP: Change `maxMonsterHP` value
- Damage multipliers: Adjust the damage calculation in `handleCorrectSpelling()`
- Monsters per level: Change `monstersRemaining` initial value

## Tips for Best Experience

1. **Use Headphones**: Better audio quality for pronunciation
2. **Full Screen**: Play in full screen for best visuals
3. **Mobile**: Works great on tablets with the responsive design
4. **Practice**: Replay levels to improve your accuracy
5. **Build Combos**: Try to get long streaks for high scores

## Future Enhancements

Possible additions:
- Leaderboard system
- Timed challenges
- More word categories (Biology, History, etc.)
- Difficulty customization
- Multiplayer mode
- Sound effects and background music
- Achievement badges
- Daily challenges

## License

Feel free to use, modify, and share this game for educational purposes.

Enjoy learning English the fun way! 🎮📚✏️

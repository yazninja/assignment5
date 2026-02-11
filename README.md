# DevOps Hangman - Bug Detection Lab

## 🎯 Your Mission

A development team has created a DevOps-themed Hangman game for training new engineers. The game appears to work, but early testers reported "something feels off." Your job is to **thoroughly test the application** and identify all bugs before it's deployed.

## 📋 Testing Approach

**Use the REQUIREMENTS.md file as your guide!** This document defines exactly how the application SHOULD behave. Compare the actual behavior to the requirements to identify bugs.

---

## 📖 Game Description

### What is DevOps Hangman?

A two-player word-guessing game where players take turns guessing DevOps-related terms. Learn terminology while competing with a friend!

### Features

✅ **Two-Player Gameplay**
- Players enter their names
- Take turns guessing letters
- Score points for successful rounds
- 6 wrong guesses allowed per round

✅ **Word Bank Management**
- Pre-loaded with 20 DevOps terms
- Add your own words
- Edit existing words
- Delete unwanted words
- Changes saved automatically

✅ **Classic Mechanics**
- Click letters to guess
- Correct letters fill in blanks
- Wrong guesses draw the hangman
- Track lives and wrong letters
- Win by completing the word (10 points)
- Lose by running out of lives

---

## 🚀 How to Play

### Setup
1. Open `index.html` in your web browser
2. Enter Player 1's name in first box
3. Enter Player 2's name in second box
4. Click "Start Game"

### Playing
1. Current player is highlighted in green
2. Click alphabet letters to guess
3. Correct letters appear in the word
4. Wrong letters draw hangman and appear below
5. Win the round: Get 10 points
6. Lose the round: Next player's turn
7. Click "Next Round" to continue

### Managing Words
1. Click "Word Bank" tab
2. View all available words
3. Type new word and click "Add Word"
4. Click "Edit" or "Delete" for existing words
5. Switch back to "Play Game" tab

---

## 🔍 What to Test

The game **appears to work** but has multiple bugs. Your goal is to find **ALL** of them.

**📋 Important: Read REQUIREMENTS.md first!** This document lists all the expected behaviors. Test each requirement and see if the application meets it.

### Areas to Focus On

#### 1. **Word Bank Management**
Test adding, editing, and deleting words:
- [ ] Can you add words?
- [ ] What happens with empty input?
- [ ] Can you add duplicates?
- [ ] Can you add numbers? Symbols? Spaces?
- [ ] Does editing work correctly?
- [ ] Does deleting remove the right word?
- [ ] Do changes save after refreshing?

#### 2. **Player Setup**
Test player name entry:
- [ ] What happens with empty names?
- [ ] Can both players have the same name?
- [ ] Do names display correctly in-game?

#### 3. **Gameplay**
Play several complete rounds:
- [ ] Do correct guesses work?
- [ ] Do wrong guesses work?
- [ ] Can you click the same letter twice?
- [ ] Does the hangman draw correctly?
- [ ] Are lives counted properly?
- [ ] Does the word reveal correctly?
- [ ] Does "Wrong Guesses" show the right letters?

#### 4. **Winning and Losing**
Pay close attention to game outcomes:
- [ ] Who gets points when someone wins?
- [ ] Does the right player's name appear in the message?
- [ ] What color is the win message? Loss message?
- [ ] Who plays the next round?
- [ ] Do players take turns?

#### 5. **Game Flow**
Test the overall experience:
- [ ] Can the same word appear twice?
- [ ] Can you switch tabs during a game?
- [ ] What happens when word bank is empty?
- [ ] Does everything persist after page refresh?

---

## 🛠️ Testing Tools

### Browser Developer Tools (Press F12)

**Console Tab**
- Watch for JavaScript errors
- Red text indicates problems
- Check for warnings

**Application Tab**
- Navigate to "Local Storage"
- Check what data is being saved
- Verify keys and values

**Elements Tab**
- Inspect HTML structure
- Check CSS classes being applied
- Verify element visibility

**Network Tab**
- Not needed (no server calls)

---

## 📝 Bug Report Template

Document each bug using this format:

```markdown
========================================
BUG #[Number]
========================================

TITLE: [Short descriptive title]

FILE: [index.html / styles.css / script.js]

LOCATION: [Approximate line number or function name if known]

DESCRIPTION:
[Clear explanation of what's wrong]

STEPS TO REPRODUCE:
1. [First action]
2. [Second action]
3. [What happens]

EXPECTED BEHAVIOR:
[What SHOULD happen]

ACTUAL BEHAVIOR:
[What ACTUALLY happens]

SEVERITY:
[ ] Critical - Game is unplayable
[ ] High - Major feature broken
[ ] Medium - Feature works but incorrectly
[ ] Low - Minor issue or cosmetic

SUGGESTED FIX: [Optional - bonus points!]
========================================
```

---

## 💡 Testing Tips

### Think Like a Player
- Play the game naturally first
- Try to win AND lose
- Switch between players
- Use the word bank features
- Notice anything that feels "wrong"

### Think Like a Hacker
- Try to break things
- Enter invalid data
- Click rapidly
- Test edge cases
- Do unexpected things

### Think Like a Developer
- Read the source code (right-click → View Source)
- Check the console for errors
- Look at localStorage in DevTools
- Verify variable names and logic
- Trace what happens when you click

### Common Bug Patterns
- **Wrong values**: Scores, names, or data going to wrong places
- **Missing validation**: No checks for invalid input
- **Off-by-one errors**: Array index mistakes
- **Display issues**: Wrong colors, text, or visibility
- **State management**: Data not saving or updating
- **Logic errors**: Conditions that are incorrect

---

## ✅ Testing Checklist

### Quick Tests (Do These First)
- [ ] Play one complete round from start to finish
- [ ] Win a round and observe what happens
- [ ] Add a blank word to the word bank
- [ ] Delete a word from the middle of the list
- [ ] Make 6 wrong guesses
- [ ] Refresh the page and check if changes saved

### Thorough Tests
- [ ] Play 5+ rounds and track scores carefully
- [ ] Test every letter in the alphabet
- [ ] Add 10 different test words (valid and invalid)
- [ ] Edit and delete multiple words
- [ ] Win 3 rounds with Player 1, observe scores
- [ ] Lose 3 rounds with Player 2, observe scores
- [ ] Switch tabs multiple times during gameplay

### Edge Cases
- [ ] Start game with no player names
- [ ] Add word with only spaces
- [ ] Add word with numbers: "DEVOPS123"
- [ ] Add word with symbols: "DEV-OPS"
- [ ] Delete the first word in the list
- [ ] Delete the last word in the list
- [ ] Click the same letter 5 times
- [ ] Play with only 2 words in bank

---

## 🎓 Learning Objectives

By completing this lab, you will:
- Practice systematic software testing
- Learn to use browser DevTools effectively
- Understand common web application bugs
- Identify validation and logic errors
- Learn DevOps terminology
- Develop debugging skills
- Write clear bug reports

---

## ⚠️ Important Notes

1. **The game IS playable** - You can complete full rounds despite bugs
2. **Some bugs are obvious** - You'll notice them immediately
3. **Some bugs are subtle** - Requires careful observation
4. **Some bugs are hidden** - Need code review to find
5. **Test systematically** - Don't just play casually
6. **Document everything** - Even small issues matter

---

## 🏆 Challenge Goals

- **Bronze**: Find 6+ bugs (basic testing)
- **Silver**: Find 10+ bugs (thorough testing)
- **Gold**: Find 15+ bugs (excellent testing)
- **Platinum**: Find all bugs + suggest fixes (outstanding work)

---

## 📚 DevOps Terms to Know

While testing, you'll encounter these terms. Make sure you understand them:

| Term | Meaning |
|------|---------|
| **DevOps** | Development + Operations culture |
| **Agile** | Iterative development methodology |
| **CI/CD** | Continuous Integration / Deployment |
| **Pipeline** | Automated build/deploy process |
| **Docker** | Containerization platform |
| **Scrum** | Agile framework with sprints and ceremonies |
| **Kanban** | Visual workflow management method |
| **Git** | Version control system |
| **Branch** | Parallel development line |
| **Commit** | Save changes to repository |
| **Merge** | Combine code branches |
| **Deploy** | Release to production |
| **Hotfix** | Urgent production bug fix |
| **Testing** | Verify code correctness |
| **Snapshot** | Point-in-time backup |

---

## 🚀 Ready to Begin?

1. Open `index.html` in your browser
2. Read through the game instructions
3. Start testing systematically
4. Document every bug you find
5. Think critically about each issue
6. Have fun bug hunting!

**Remember**: The best testers don't just find bugs - they understand WHY the bugs happen and HOW to fix them!

Good luck! 🐛🔍

---

## 💬 Questions to Ask Yourself

As you test, consider:
- Does this behavior make sense?
- Is the displayed information correct?
- Are the right things happening at the right time?
- Could this cause problems for users?
- Is data being saved and loaded correctly?
- Are there any security or cheating concerns?
- Does the UI provide proper feedback?
- Are error messages helpful?

Think like a QA engineer - question everything!

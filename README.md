A JavaFX-based tower defense game project created for CSC-2592-98533, where you defend against waves of enemies using different types of towers.

**Initial game with two towers placed**
![Initial Game Image](https://github.com/Chloe161200/TowerDefense/blob/main/src/main/resources/images/game1.png?raw=true "Game image with towers placed")

## Development Team

- **Jayden**: Base Code, Git Hub, & AI
- **Joe**: UI & Game Effects
- **Chloe**: Tester & Website Developer
- **Charles**: Tester & UI Elements


## Features

- 🏰 **Multiple tower types** with unique ranges, damage, and abilities  
- 👾 **Advanced enemy system** with Camo, Armored, Regenerating, and Boss enemies  
- 🌊 **Wave-based progression** with increasing difficulty  
- 🧱 **Interactive tower placement** and in-game management tools  
- 📈 **Score tracking & leaderboard** backed by a local SQLite database  
- 🎨 **Visual effects and animations** built with JavaFX  
- 🗄️ **Local SQLite database** for high scores

**Showcasing the Leaderboard**
![Leaderboard](https://github.com/Chloe161200/TowerDefense/blob/main/src/main/resources/images/game2.png?raw=true "Game image leaderboard")

## Requirements

- Java 17 or higher
- JavaFX
- Maven

## How to Run

1. Clone this repository
2. Navigate to the project directory
3. Run the following commands:

```bash
mvn clean install
mvn javafx:run
```

## Game Controls

- Left-click on towers to view their range
- Right-click on towers to sell them (50% refund)
- Place towers by selecting them from the tower panel
- Monitor your health, money, and score in the game UI

## Tower Types

1. **Basic Tower**
   - Cost: 50
   - Balanced range and damage
   - Medium attack speed
  
![Basic Tower](https://github.com/Chloe161200/TowerDefense/blob/main/src/main/resources/images/BasicTower.gif?raw=true "Game image with tower radius")

2. **Sniper Tower**
   - Cost: 100
   - Very long range, high damage
   - Can detect camo enemies
   - Slow attack speed

3. **Machine Gun Tower**
   - Cost: 150
   - Short range, low damage per shot
   - Very fast attack speed
  
**Each tower has its own radius**
![Tower Radius](https://github.com/Chloe161200/TowerDefense/blob/main/src/main/resources/images/game3.png?raw=true "Game image with tower radius")

## Enemy Types

- **Normal**: Basic enemies
- **Camo**: Can only be detected by certain towers
- **Armored**: Takes reduced damage
- **Regenerating**: Heals over time
- **Boss**: Appears every 10 waves with multiple special properties

## Game Rules

- Defend against increasingly difficult waves of enemies
- Don't let enemies reach the end of the path
- Earn money by defeating enemies
- Place towers strategically to handle different enemy types
- Try to achieve the highest score possible!






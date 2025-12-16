A JavaFX-based tower defense game project created for CSC-2592-98533, where you defend against waves of enemies using different types of towers.

**Initial game with two towers placed**
![Initial Game Image](https://github.com/Chloe161200/TowerDefense/blob/main/src/main/resources/images/game1.png?raw=true "Game image with towers placed")

## Development Team

- **Jayden**: Base Code, Git Hub Repository, & AI
- **Joe**: UI & Buffing System
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

## Tower Constructor - Code

This code shows how different tower types are created and configured using a single Tower constructor. Based on the tower type, the constructor assigns values such as cost, range, damage, attack speed, and special abilities like camo detection, while also loading the correct image and visual effects. This approach makes it easy to manage multiple tower behaviors while keeping the code organized and reusable.

```bash
public Tower(double x, double y, String type, double mapWidth, double mapHeight) {
   this.x = x;
   this.y = y;
   this.towerType = type;
   this.towerSize = mapHeight * 0.05;
   String imagePath;
   switch (type.toLowerCase()) {
      case "sniper":
         this.cost = 100;
         this.range = 2.0 * Math.min(mapWidth, mapHeight) * 0.2;
         this.damage = 50.0;
         this.attackSpeed = 0.5;
         this.projectileColor = Color.RED;
         imagePath = this.getClass().getClassLoader().getResource("images/sniper_tower.png").toString();
         this.sprite = new Image(imagePath);
         this.canSeeCamo = true;
         break;
      case "machine":
         this.cost = 150;
         this.range = 1.0 * Math.min(mapWidth, mapHeight) * 0.2;
         this.damage = 10.0;
         this.attackSpeed = 3.0;
         this.projectileColor = Color.LIGHTGREEN;
         imagePath = this.getClass().getClassLoader().getResource("images/rapid_tower.png").toString();
         this.sprite = new Image(imagePath);
         this.canSeeCamo = false;
         break;
      default:
         this.cost = 50;
         this.range = 1.5 * Math.min(mapWidth, mapHeight) * 0.2;
         this.damage = 20.0;
         this.attackSpeed = 1.0;
         imagePath = this.getClass().getClassLoader().getResource("images/basic_tower.png").toString();
         this.sprite = new Image(imagePath);
         this.projectileColor = Color.CYAN;
         this.canSeeCamo = false;
}
```

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

## Future Work

- Add **tower upgrade systems** so players can improve damage, range, or special abilities
- Introduce **new tower types**, such as support towers that boost nearby towers or slow enemies
- Expand the **enemy variety**, including enemies that split when defeated or temporarily disable towers
- Improve **visual effects and animations** to better show enemy abilities and tower attacks
- Add **sound effects and background music** to make gameplay more immersive








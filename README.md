Documentation for Mario Game
________________________________________
Game Overview
This game is a 2D platformer where the player controls a character (similar to Mario) that can jump, run, and collect coins while avoiding obstacles and platforms. The game includes a score system that rewards the player with points for collecting coins. The game ends when the player falls off the screen, and a "Game Over" screen is displayed. If the player reaches a certain score, a "Win" screen is shown.
________________________________________
Game Features
1.	Player Movement:
o	The player can move left and right using the arrow keys.
o	The player can jump using the up arrow key.
o	The player is affected by gravity and falls if they are not on a platform.
2.	Platforms:
o	Static platforms are placed across the screen, which the player can jump on.
o	Hills are also placed as decorative elements.
3.	Coins:
o	Collectable items (coins) are scattered throughout the level.
o	The player earns points for each coin collected.
4.	Game States:
o	Start Screen: Displays a start button to begin the game.
o	Game Over Screen: Appears when the player falls off the screen.
o	Win Screen: Appears when the player collects enough coins to win the game 
5.	Score System:
o	The player gains 10 points for each coin collected.
o	The score is displayed at the top-left corner of the screen.
o	The game ends when the player falls off the screen, and the score is shown on the "Game Over" screen.
________________________________________
Game Components
1. Player Class
The Player class defines the player's character and behavior.
•	Properties:
o	position: The position of the player on the canvas (x, y).
o	velocity: The movement velocity of the player (x, y).
o	width: The width of the player character.
o	height: The height of the player character.
o	image: The sprite image of the player.
o	frames: The current frame of the animation.
o	isJumping: Boolean indicating if the player is in the air.
o	sprites: An object containing images for different actions (standing, running).
•	Methods:
o	draw(): Draws the player's current sprite at their position.
o	update(): Updates the player's movement, applies gravity, and handles jumping.
o	jump(): Makes the player jump if they are not already jumping.
2. Coin Class
The Coin class represents collectible coins in the game.
•	Properties:
o	position: The position of the coin on the canvas (x, y).
o	width: The width of the coin.
o	height: The height of the coin.
o	image: The image of the coin (if available).
•	Methods:
o	draw(): Draws the coin on the canvas.
3. Platform Class
The Platform class represents static platforms in the game.
•	Properties:
o	position: The position of the platform on the canvas (x, y).
o	width: The width of the platform.
o	height: The height of the platform.
o	image: The image used for the platform.
•	Methods:
o	draw(): Draws the platform on the canvas.
4. PlatformHill Class
The PlatformHill class represents hills in the game that the player can jump on.
•	Properties:
o	position: The position of the hill on the canvas (x, y).
o	width: The width of the hill.
o	height: The height of the hill.
o	image: The image used for the hill.
•	Methods:
o	draw(): Draws the hill on the canvas.
5. GenericObject Class
The genericObject class is used for non-interactive objects, such as the background or scenery.
•	Properties:
o	position: The position of the object on the canvas (x, y).
o	image: The image used for the object.
•	Methods:
o	draw(): Draws the object on the canvas.
________________________________________
Game Logic
1.	Starting the Game:
o	When the player clicks the "Start" button, the game begins, and the start screen is hidden.
o	The start() function initializes the game objects and starts the game loop.
2.	Movement:
o	The player can move left or right using the arrow keys. The velocity is updated based on key presses.
o	The update() method of the Player class handles gravity, jumping, and movement.
o	The jump() method makes the player jump by changing the velocity.y.
3.	Coin Collection:
o	The checkCoinCollision() function checks if the player’s bounding box overlaps with a coin’s bounding box. If they collide, the coin is removed, and the score is incremented by 10.
4.	Platforms:
o	The player’s position is checked against each platform to see if they are landing on one. If the player is falling onto a platform, their velocity.y is set to 0, and they are no longer considered "jumping."
5.	Game Over:
o	If the player’s position goes below the canvas height (i.e., they fall off the screen), the game ends, and the "Game Over" screen is shown.
o	The gameOver() function is called, and the gameOverSound is played.
________________________________________
Controls
•	Arrow Up (↑): Jump
•	Arrow Left (←): Move left
•	Arrow Right (→): Move right
________________________________________
Audio
The game uses the following sound effects:
•	startSound: Played when the game starts.
•	jumpSound: Played when the player jumps.
•	coinSound: Played when the player collects a coin.
•	gameOverSound: Played when the game is over.
________________________________________
File Structure
•	HTML Files:
o	index.html: The main HTML file containing the canvas and game controls.
•	Image Files:
o	background.png: The background image for the game.
o	platform.png: The platform image.
o	coin.png: The image for the collectible coin.
o	player.png: The sprite image for the player (standing, running).
•	Sound Files:
o	gamestart-272829.mp3: Sound played when the game starts.
o	smb_jump-small.wav: Sound played when the player jumps.
o	smb_coin.wav: Sound played when the player collects a coin.
o	smb_gameover.wav: Sound played when the game ends.
________________________________________

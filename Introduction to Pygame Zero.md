1. Creating a window
	Command for running pygame .py file
	`pgzrun intro.py`

2. Drawing a background
	```
	# intro.py
	WIDTH = 300
	HEIGHT = 300
	
	def draw():
		screen.fill((128, 0, 0))  
	```
	
	`screen`  is an object.
	`screen.fill()` is a method call.
	`(128, 0, 0)` is a colour tuple（元组）
	

3. Draw a sprite
	"alpha" channel: transparency channel for an image.
	`images/` is the standard directory for Pygame Zero images.

	```
	# intro.py
	alien = Actor('alien')
	alien.pos = 100, 56

	WIDTH = 500
	HEIGHT = alien.height + 20

	def draw():
	    screen.clear()
	    alien.draw()
	```
	passing the string `'alien'` to the `Actor` class
	`HEIGHT` of the window is set based on the height of the alien.
	`alien.draw()` is a method draws the sprite

4. Moving the alien
	`alien.topright = 0, 10`
	assign to `topright` to move the alien actor by its top-right corner.

	```
	def update():
	    alien.left += 2
	    if alien.left > WIDTH:
	        alien.right = 0
	```
	Pygame Zero will call your `update()` function once every frame.
	The `draw()` function draws the current position of the alien while the `update()` function is used to show the alien moving on the screen.

5. Handling clicks
	





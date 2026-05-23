DArk GAME:

JAVASCRIPT:
**The program starts with a some generalised definations:**

  We get canvas element from the HTML.
  A 2D canvas kit.
  we get elements have to be updated in game.
  we define the room properties and sizes using mathematics.
  we define arrays one to store the room and enemy locations and other to store acive bullets.
  we define game states like pause and gameover are 0.
  we define health and score variable too.

**We first have the start() function: (ROOM GENERATION LOGIC)**

  this function makes the rooms in proper geometry and puts the enemies into it.
  after drawing these it puts this data as array in MAP making it a 2D array.
  after calculating the room size and gaps between the rooms we move to building it using the loop.
  we use canvas API's fill rect function and move with to top left corner of each room and build sqaure of size define in above.
  we take a random number to randomly place a door of height and width calculated initially in the room.
  after every iteration we do new position of rect is x= j*(sqauresize)+adjusted gap for x (column we are making for is j).
                                                      y= i*(sqauresize)+adjusted gap for y (row we are making for is i).
	we find center of room and set enemy little away from it.
	saving this coordinates in our MAP array.

**we have then defined a chkrect() function:**

  this function stands for checking rectangle.
  it takes in a point of cordinates (fx,fy), rectangle(room) coordinates (rx,ry), and room door's dimensions (rw,rh).
  Using basic mathematics of distances and logical expression.
    it return 1 if point inside room.
    it return 0 if point outside room.
  it returns 0 if we are on the door too.

**After this function we defined another important function chkcoli() function:**


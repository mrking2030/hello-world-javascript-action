/* Karel paints a U.S. flag on the 40x40 canvas along with the letters U.S.A.
/* programmed by Mr. King at New Designs Charter School. */
function start(){
    moveToFlagCorner();
 /* Karel paints the star area on the flag. */
        for (var i = 0; i < 4; i++){
            flagFiveStarRow();
            move();
            flagSixStarRow();
        }
    flagFiveStarRow();
    turnAround();
    moveToFlagCorner();

/* Karel paints the short red stripes on the flag. */
        for (var i = 0; i < 2; i++){
            flagRedStripeRightShort();
            flagRedStripeLeftShort();
        }
    flagRedStripeRightShort();
    
/* Karel paints the long red stripes on the flag. */
    flagRedStripeLeftLong();
    flagRedStripeRightLong();
    flagRedStripeLeftLong();

/* Karel paints the U.S.A. letters. */
    turnRight();
    move();
    UForUnited();
    SForStates();
    AForAmerica();
}

/* Karel moves to the top of the canvas readying himself to paint the flag. */
function moveToFlagCorner(){
    turnLeft();
    while(frontIsClear()){
        move();
    }
    turnAround();
    move();
    move();
    turnLeft();
}

/* Karel paints a five white star/square, six blue square row on the flag 
moving from left to right and sets up to paint the next row below readying 
to move right to left. */
function flagFiveStarRow(){
    for (var i = 0; i < 6; i++){
        move();
        paint(Color.blue);
        move();
    }
    turnRight();
    if(frontIsClear()){
        move();
    }
    turnRight();
}

/* Karel paints a six white star/square, five blue square row on the flag 
moving from right to left and sets up to paint the next row below readying
to move left to right. */
function flagSixStarRow(){
    for (var i = 0; i < 5; i++){
        move();
        paint(Color.blue);
        move();
    }
    move();
    turnLeft();
    if(frontIsClear()){
        move();
    }
    turnLeft();
}

/* Karel paints a 16 unit long red stripe in the flag moving from left to 
right on the canvas. */
function flagRedStripeRightShort(){
    for (var i = 0; i < 16; i++){
        if(frontIsClear()){
            paint(Color.red);
            move();
        }
    }
    turnRight();
    move();
    move();
    turnRight();
    move();
}

/* Karel paints a 16 unit long red stripe in the flag moving from right to 
left on the canvas. */
function flagRedStripeLeftShort(){
    for (var i = 0; i < 16; i++){
        if(frontIsClear()){
            paint(Color.red);
            move();
        }
    }
    turnLeft();
    move();
    move();
    turnLeft();
    move();
}

/* Karel paints a 27 unit long red stripe in the flag moving from right to 
left on the canvas. */
function flagRedStripeLeftLong(){
    for (var i = 0; i < 27; i++){
        if(frontIsClear()){
            paint(Color.red);
            move();
        }
    }
    turnLeft();
    move();
    move();
    turnLeft();
    move();
}     

/* Karel paints a 27 unit long red stripe in the flag moving from left to 
right on the canvas. */
function flagRedStripeRightLong(){
    for (var i = 0; i < 27; i++){
        if(frontIsClear()){
            paint(Color.red);
            move();
        }
    }
    turnRight();
    move();
    move();
    turnRight();
    move();
}    

/* Karel paints a letter "U" for United in red. */
function UForUnited(){
    for (var i = 0; i < 14; i++){
        paint(Color.red);
        move();
    }
    turnLeft();
    for (var i = 0; i < 8; i++){
        paint(Color.red)
        move();
    }
    turnLeft();
    for (var i = 0; i < 15; i++){
        paint(Color.red);
        move();
    }
    turnRight();
}

/* Karel paints a letter "S" for States in alternating red & blue. */
function SForStates(){
    for (var i = 0; i < 11; i++){
        move();
    }
    turnRight();
    move();
    turnRight();
    for (var i = 0; i < 4; i++){
        paint(Color.blue);
        move();
        paint(Color.red);
        move();
    }
    paint(Color.blue);
    turnLeft();
    for (var i = 0; i < 3; i++){
        move();
        paint(Color.red);
        move();
        paint(Color.blue);
    }
    move();
    turnLeft();
    for (var i = 0; i < 4; i++){
        paint(Color.red);
        move();
        paint(Color.blue);
        move();
    }
    paint(Color.red);
    turnRight();
        for (var i = 0; i < 3; i++){
        move();
        paint(Color.blue);
        move();
        paint(Color.red);
    }
    move();
    turnRight();
    for (var i = 0; i < 4; i++){
        paint(Color.blue);
        move();
        paint(Color.red);
        move();
    }        
        paint(Color.blue);
    turnLeft();
    move();
    turnLeft();
}

/* Karel paints a letter "A" for America in blue. */
function AForAmerica(){
    for (var i = 0; i < 11; i++){
        move();
    }
    turnLeft();
    move();
    for (var i = 0; i < 7; i++){
        paint(Color.blue);
        move();
        paint(Color.blue);
        move();
        turnRight();
        move();
        turnLeft();
    }
    turnLeft();
    move();
    paint(Color.blue);
    turnLeft();
    move();
    move();
    for (var i = 0; i < 6; i++){
        move();
        turnLeft();
        move();
        turnRight();
        paint(Color.blue);
        move();
        paint(Color.blue);
    }
    turnRight();
    for (var i = 0; i < 3; i++){
        move();
    }
    turnRight();
    for (var i = 0; i < 6; i++){
        move();
    }
    turnLeft();
    move();
    for (var i = 0; i < 5; i++){
        paint(Color.blue)
        move();
    }
}


/* Karel paints a line repeating red and blue again and again across any size
canvas with blank spaces in between moving from right to left. Also, he sets 
up on the next row above to paint again moving next from left to right. Together
with AmericaLeft(); looped Karel paints the entire canvas red, white, and blue.
*/
function AmericaLeft(){
    while(frontIsClear()){
        paint(Color.red);
        if(frontIsClear()){
            move();
        } 
        if(frontIsClear()){
            move();
        }    
        paint(Color.blue);
        if(frontIsClear()){
            move();
        }
        if(frontIsClear()){
            move();
        }    
    }
    turnRight();
    if(frontIsClear()){
        move();
    }
    turnRight();
}


/* Karel paints a line repeating red and blue again and again across any size
canvas with blank spaces in between moving from left to right. Also, he sets 
up on the next row above to paint again moving next from right to left. Together
with AmericaLeft(); looped Karel paints the entire canvas red, white, and blue.
*/
function AmericaRight(){
    while(frontIsClear()){
        paint(Color.red);
        if(frontIsClear()){
            move();
        }
        if(frontIsClear()){
            move();
        }
        paint(Color.blue);
        if(frontIsClear()){
            move();
        }
        if(frontIsClear()){
            move();
        }
    }
    turnLeft();
    if(frontIsClear()){
        move();
    }
    turnLeft();
}

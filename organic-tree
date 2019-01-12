float angleMax=PI/3.5;
//float angleMiddle=0;
float angleMin=-PI/3.5;
float ratioMax=.86;
float ratioMin=.3;
color leaf=color(0, 110, 30, 100);
color branch=color(89, 49, 0, 150);
boolean go;
void setup() {
  size(800, 800);
  background(0);
  stroke(branch);
  go=true;
  rectMode(CENTER);
    
}

void draw() {

  if (go) {
    translate(0, height+20);
    background(0);

      stroke(branch);
   

      pushMatrix();
  
      translate(width/2,0);
      branch(random(150, 250));
      popMatrix();

  }
  go=false;
}

void keyPressed() {
  go=true;
}

void mousePressed() {
  saveFrame("####.png");
  println("Saved");
}

void branch(float len) {
  if (len>=1) {
    
    noStroke();
    fill(branch);
    
    translate(0, -len/2);
    rect(0,0,len/8,len);
    translate(0, -len/2);
    
    stroke(150,100);
    for (int x=0; x<int(random(3, 6)); x++) {
      
      pushMatrix();
      rotate(random(angleMin, angleMax));
      
      branch(len*random(ratioMin, ratioMax));
      
      popMatrix();
     
    }
  }
  else {

    stroke(leaf);
    //noStroke();
    point(0, 0);
    stroke(branch);
  }
}

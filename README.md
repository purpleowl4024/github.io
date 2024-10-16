boolean running = true;

void setup() {
  size(400, 400);
}

void draw() {
  background(200);

  // Draw the stop button
  fill(255, 0, 0);
  rect(150, 170, 100, 60);
  fill(255);
  textAlign(CENTER, CENTER);
  textSize(20);
  text("Stop", 200, 200);

  if (running) {
    // Your main sketch code goes here
    // Example: Animate a circle
    fill(0, 100, 255);
    ellipse(frameCount % width, height / 2, 50, 50);
  }
}

void mousePressed() {
  // Check if the stop button is clicked
  if (mouseX > 150 && mouseX < 250 && mouseY > 170 && mouseY < 230) {
    running = false;
  }
}

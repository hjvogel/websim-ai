# WebSim-AI

Welcome to the WebSim-AI repository! Here, you'll find a collection of pages and tools designed to demonstrate various simulations and games, all built to showcase the capabilities of modern web technologies and AI integrations.

## Check Out My Stuff Running

Explore live demos and experiments currently hosted on WebSim-AI:

[WebSim-AI @ Collab](https://websim.ai/@Collab)

## Try Out These Tools and Games

### [Croquet Portal](https://profi-thon-site.vercel.app/CroquetPortal.html)
Dive into an interactive 3D environment that showcases the potential of collaborative simulations using Croquet, a powerful platform for building multiplayer applications.

### [Magic Worm](https://profi-thon-site.vercel.app/MagicWorm.html)
Experience the classic game of Snake with a magical twist. Control the worm, collect items, and grow longer while avoiding obstacles.

### [Tetris GH](https://profi-thon-site.vercel.app/Tetris_GH.html)
Play a modern web-based version of the timeless game Tetris. Arrange the falling blocks to clear lines and score points in this addictive puzzle game.

### [Wood Block](https://profi-thon-site.vercel.app/WoodBlock.html)
Enjoy a relaxing and challenging puzzle game where you need to fit wooden blocks into a grid. Test your spatial reasoning and problem-solving skills.

### [WebSim 2D Robo](https://profi-thon-site.vercel.app/WebSim2D.html)
Explore 2D Robo code simulations powered by WebSim. Experiment with different scenarios and observe how various parameters affect the outcomes.

eg try out pasing in that Robo Code 

// Advanced robot control code
function exploreEnvironment() {
  if (goal) {
    // Calculate angle to goal
    const dx = goal.x - robotX;
    const dy = goal.y - robotY;
    const angleToGoal = Math.atan2(dy, dx);
    
    // Calculate difference between current angle and angle to goal
    let angleDiff = angleToGoal - robotAngle;
    
    // Normalize angle difference to [-PI, PI]
    while (angleDiff > Math.PI) angleDiff -= 2 * Math.PI;
    while (angleDiff < -Math.PI) angleDiff +=  Math.PI;
    
    if (Math.abs(angleDiff) > 0.1) {
      // Turn towards goal
      robot.setVelocity(0, angleDiff > 0 ? 0.5 : -0.3);
      robot.setVelocity(0.5, 0);

    } else if (!robot.detectObstacle()) {
      // Move towards goal
      robot.setVelocity(0.5, 0);
    } else {
      // Obstacle avoidance
      robot.setVelocity(0, -0.3);
      robot.setVelocity(0.5, 0);

    }
  } else {
    // No goal, just explore
    if (!robot.detectObstacle()) {
      robot.setVelocity(0.5, 0);
    } else {
      robot.setVelocity(0, -0.3);
      robot.setVelocity(0.5, 0);

    }
  }
}

// Start exploration for 10 seconds
robot.run(exploreEnvironment, 10000);
        

## Record of Run - Missing Full Accounted to Really RoAR

Keep track of the various simulations and games you try out. Note that a full account of runs is currently not implemented, but you can still explore and enjoy the available features.

Feel free to reach out if you have any questions or suggestions. Enjoy exploring WebSim-AI!

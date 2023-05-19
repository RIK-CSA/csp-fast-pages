---
title: Better Python 2D Iteration and Animations
toc: true
categories: [week34, tri3]
image: /images/javascript.png
badges: true
comments: true
author: Raunak Mondal
description: Working with 2D elements and working with animations
---
<head>
    <title>Projectile Motion Simulation</title>
    <style>
      #canvas {
        border: 1px solid #000;
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <canvas id="canvas" width="800" height="400"></canvas>

    <script>
      // Function to draw the projectile on the canvas
      function drawProjectile(context, x, y) {
        context.beginPath();
        context.arc(x, y, 10, 0, 2 * Math.PI);
        context.fillStyle = "#FF0000";
        context.fill();
        context.closePath();
      }

      // Function to simulate the projectile motion
      function simulateProjectileMotion(canvas, initialVelocity, angle) {
        var context = canvas.getContext("2d");
        var time = 0;
        var timeInterval = 0.05; // Change this value to adjust the time interval

        // Calculate initial velocity components
        var velocityX = initialVelocity * Math.cos(angle);
        var velocityY = initialVelocity * Math.sin(angle);

        // Calculate initial position
        var x = 0;
        var y = canvas.height;

        function animationLoop() {
          context.clearRect(0, 0, canvas.width, canvas.height);

          // Calculate new position
          x = velocityX * time;
          y = canvas.height - velocityY * time + 0.5 * 9.81 * Math.pow(time, 2);

          // Draw the projectile
          drawProjectile(context, x, y);

          time += timeInterval;

          // Continue animation until the projectile hits the ground
          if (y < canvas.height) {
            requestAnimationFrame(animationLoop);
          }
        }

        animationLoop();
      }

      // Run the simulation when the page loads
      window.onload = function () {
        var canvas = document.getElementById("canvas");
        simulateProjectileMotion(canvas, 50, Math.PI / 4); // Adjust the initialVelocity and angle as desired
      };
    </script>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Draw a Dog</title>
</head>
<body>

<canvas id="dogCanvas" width="500" height="500"></canvas>

<script>
    // Get the canvas and context
    const canvas = document.getElementById('dogCanvas');
    const ctx = canvas.getContext('2d');

    // Function to draw the dog
    function drawDog() {
        // Draw the dog's body
        ctx.beginPath();
        ctx.ellipse(250, 300, 120, 80, Math.PI / 2, 0, 2 * Math.PI);
        ctx.fillStyle = 'saddlebrown';
        ctx.fill();
        ctx.closePath();

        // Draw the dog's head
        ctx.beginPath();
        ctx.arc(250, 180, 60, 0, 2 * Math.PI);
        ctx.fillStyle = 'saddlebrown';
        ctx.fill();
        ctx.closePath();

        // Draw the dog's eyes
        ctx.beginPath();
        ctx.arc(230, 170, 10, 0, 2 * Math.PI); // Left eye
        ctx.arc(270, 170, 10, 0, 2 * Math.PI); // Right eye
        ctx.fillStyle = 'white';
        ctx.fill();
        ctx.closePath();

        // Draw the dog's nose
        ctx.beginPath();
        ctx.arc(250, 200, 8, 0, 2 * Math.PI);
        ctx.fillStyle = 'black';
        ctx.fill();
        ctx.closePath();

        // Draw the dog's mouth
        ctx.beginPath();
        ctx.arc(250, 210, 20, 0, Math.PI);
        ctx.strokeStyle = 'black';
        ctx.lineWidth = 2;
        ctx.stroke();
        ctx.closePath();

        // Draw the dog's ears
        ctx.beginPath();
        ctx.moveTo(190, 130);
        ctx.lineTo(160, 100);
        ctx.lineTo(190,


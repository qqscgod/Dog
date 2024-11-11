<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Slideshow</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        .slideshow-container {
            position: relative;
            max-width: 1000px;
            margin: 0 auto;
            overflow: hidden;
        }

        .slides {
            display: flex;
            transition: transform 1s ease;
        }

        .slide {
            min-width: 100%;
            box-sizing: border-box;
        }

        .slide img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Navigation Buttons */
        .prev, .next {
            position: absolute;
            top: 50%;
            padding: 16px;
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 50%;
            z-index: 1;
            transform: translateY(-50%);
        }

        .prev {
            left: 10px;
        }

        .next {
            right: 10px;
        }

        /* Dots Navigation */
        .dot-container {
            text-align: center;
            padding: 10px;
        }

        .dot {
            height: 15px;
            width: 15px;
            margin: 0 5px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
            cursor: pointer;
        }

        .active {
            background-color: #717171;
        }
    </style>
</head>
<body>

<div class="slideshow-container">
    <!-- Slides -->
    <div class="slides">
        <div class="slide">
            <img src="https://via.placeholder.com/1000x400/ff7f7f/333333?text=Image+1" alt="Slide 1">
        </div>
        <div class="slide">
            <img src="https://via.placeholder.com/1000x400/ffbf00/333333?text=Image+2" alt="Slide 2">
        </div>
        <div class="slide">
            <img src="https://via.placeholder.com/1000x400/4CAF50/333333?text=Image+3" alt="Slide 3">
        </div>
    </div>

    <!-- Navigation Buttons -->
    <button class="prev" onclick="moveSlide(-1)">&#10094;</button>
    <button class="next" onclick="moveSlide(1)">&#10095;</button>
</div>

<!-- Dots for Navigation -->
<div class="dot-container">
    <span class="dot" onclick="currentSlide(1)"></span>
    <span class="dot" onclick="currentSlide(2)"></span>
    <span class="dot" onclick="currentSlide(3)"></span>
</div>

<script>
    let currentSlideIndex = 1;
    let slides = document.querySelectorAll('.slide');
    let dots = document.querySelectorAll('.dot');

    // Function to move to the next or previous slide
    function moveSlide(n) {
        showSlide(currentSlideIndex += n);
    }

    // Function to show the slide based on the index
    function currentSlide(n) {
        showSlide(currentSlideIndex = n);
    }

    // Function to display the correct slide
    function showSlide(n) {
        if (n > slides.length) { currentSlideIndex = 1 }
        if (n < 1) { currentSlideIndex = slides.length }

        // Hide all slides
        for (let slide of slides) {
            slide.style.display = 'none';
        }

        // Remove the active class from all dots
        for (let dot of dots) {
            dot.classList.remove('active');
        }

        // Show the current slide and highlight the corresponding dot
        slides[currentSlideIndex - 1].style.display = 'block';
        dots[currentSlideIndex - 1].classList.add('active');
    }

    // Automatic slideshow every 3 seconds
    setInterval(function() {
        moveSlide(1);
    }, 3000);

    // Show the first slide initially
    showSlide(currentSlideIndex);
</script>

</body>
</html>

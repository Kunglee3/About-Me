<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harrison Siegel Home Page</title>
    <style>
        body {
            font-family: 'Times New Roman', Times, serif;
            background-color: #f4f4f4;
        }

        h1 {
            color: #333;
            font-size: 22px;
        }
        h2 {
            color: #333;
            font-size: 18px
        }

        p {
            color: #555;
            font-size: 16px;
        }
        .carousel-container {
            max-width: 600px; /* Adjust this to fit your desired image size */
            position: relative;
            margin: auto; /* Centers the carousel on the page */
            border: 2px solid #ddd;
            background-color: #fff; /* White background behind images */
        }

        /* Hide all slides by default */
        .carousel-slide {
            display: none;
        }

        /* Make images responsive so they fit the container */
        .carousel-slide img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Show the active slide */
        .active-slide {
            display: block;
        }
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            margin-top: -22px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
            background-color: rgba(0,0,0,0.3); /* Semi-transparent background */
            border: none; /* Removes default button border */
        }

        /* Position the "next button" to the right */
        .next {
            right: 0;
            border-radius: 3px 0 0 3px;
        }

        /* On hover, add a black background color with a little bit see-through */
        .prev:hover, .next:hover {
            background-color: rgba(0,0,0,0.8);
        }
    </style>
</head>
<body>
    <h1>Harrison Siegel</h1>
    <p>Welcome to my webpage, here you can find my contact information, resume, my past work, and what I am actively working
        on.
    </p>
    <h2>About Me</h2>
    <p>Currently I am working towards completing my masters degree of city and regional planning at the Georgia Institute of 
        Technology. I obtained my public policy bachelors degree in 2025 from the Universtiy of Kentucky and graduated magna cum
        laude. I am originally from Lexington, Kentucky and currently reside in Atlanta, Georgia. I first found my intrest in city
        planning after my first semester at the University of Kentucky. I had some familiarity with the basic concepts via a video
        game called City Skylines. Once I understood pursuing a degree in city planning was possible I changed my major from economics
        to public policy. Further into my bachelors degree I decided pursuing a masters degree will provide me with the oppertunity
        to be a city planner. I currently am involved with the Georgia Student Planning association at Georgia Tech. As an association
        we host events, workshops, class events, and much more.
    </p>
    <p>
        In my professional career I have interned with the Kentucky Transportation Cabinet, the Kentucky Public Pension 
        Authority, and Cenergistic. While working with the transportation cabinet I was working as a state highway engineering
        intern. Some of my work included the planning of a BRT route in Louisville, Kentucky, work on wrong way driving prevention
        on highway ramps, and AI camera software installation across major intersections. While working at the pension authority I
        my role was an internal auditor intern. While working I created a database for pertinant pension laws, created an internal
        audit probe on tax documents, and developed scripts to examine large databases quickly. My role at Cenergistic focused on
        energy efficiency at the University of Kentucky. As an energy specalist intern I worked on building infrastructure projects such
        as HVAC replacements, building material research, examination of energy policies held by the University, and more.
    </p>
    <p>
        For my future I plan to work in the planning field with a focus on housing, transportation, and economic development.
        I have experience with R studio, ArcGIS, Tableau, HTML, Microsoft Office, ArcPy, and Google Suite. I am 
        currently looking for any oppertunity to work in the field within the Atlanta area.
    </p>
    <h2>Contact Information</h2>
    <p>
        Phone: 859-619-2950
    </p>
    <p>
        Email: harrison.siegel03@gmail.com
    </p>
    <h2>Resume</h2>
    <p>
        You can download my resume here:
        <a href="Harrison Siegel Resume (1).pdf" download>Download Resume(PDF)</a>
    </p>
    <h2>Current Work</h2>
    <div class="carousel-container">
        <button class="prev" onclick="changeSlide(-1)">&#10094;</button>
        <button class="next" onclick="changeSlide(1)">&#10095;</button>

        <div class="carousel-slide active-slide">
            <img src="Lab 6 Q1.jpg" alt="Linear Modeling Visuals">
        </div>
        <div class="carousel-slide">
            <img src="Lab 5 Q2.2.jpg" alt="Scatter Plot">
        </div>
        <div class="carousel-slide">
            <img src="Walking Time To Grocery.jpg" alt="Walking Time In Decatur">
        </div>
        <div class="carousel-slide">
            <img src="Zoning-Decatur.jpg" alt="Zoning Within Decatur">
        </div>
    </div>
    <h2>Previous Work</h2>
    <div class="carousel-container">
        <button class="prev" onclick="changeSlide(-1)">&#10094;</button>
        <button class="next" onclick="changeSlide(1)">&#10095;</button>

        <div class="carousel-slide active-slide">
            <img src="" alt="">
        </div>
        <div class="carousel-slide">
            <img src="" alt="">
        </div>
        <div class="carousel-slide">
            <img src="" alt="">
        </div>
        <div class="carousel-slide">
            <img src="" alt="">
        </div>
    </div>
    <script>
        let currentSlideIndex = 0;
        showSlides(currentSlideIndex);
        function changeSlide(n) {
            showSlides(currentSlideIndex += n);
        }
        function showSlides(n) {
            let slides = document.getElementsByClassName("carousel-slide");
            if (n >= slides.length) { currentSlideIndex = 0 }
            if (n < 0) { currentSlideIndex = slides.length - 1 }
            for (let i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slides[currentSlideIndex].style.display = "block";
        }
    </script>
</body>
</html>
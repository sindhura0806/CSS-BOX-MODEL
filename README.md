## 📦 Day 5 – CSS Box Model
Today I learned about the CSS Box Model,
which is the foundation of layout design in web development.
# ✅ 1️⃣ What is CSS Box Model?
Every HTML element is treated as a box.
It consists of:
1.Margin
2.Padding
3.Border
4.Width

# ✅ 2️⃣ Margin
-🔹 Space outside the element -🔹 Creates gap between elements

Example:
.box { margin: 20px; }

-👉 Adds 20px space outside the element on all sides.

# ✅ 3️⃣ Padding
-🔹 Space inside the element -🔹 Between content and border

Example:
.box { padding: 15px; }

-👉 Adds space inside the box.

# ✅ 4️⃣ Border
-🔹 Surrounds padding and content

Example:
.box { border: 2px solid black; }

You can control:

border-width: 2px; border-style: solid; border-color: red;

# ✅ 5️⃣ Width vs Max-Width
🔹 width
Fixed width.

.box { width: 400px; }

-⚠️ If screen is smaller, it may overflow.

🔹 max-width
Responsive width.

.box { max-width: 400px; }

-👉 Element will shrink on smaller screens. -👉 Best for responsive design. -✅ Always prefer max-width for containers.

# ✅ 6️⃣ box-sizing Property
By default:

width = content only

Padding & border are added extra.

Example (Default: content-box)
.box { width: 200px; padding: 20px; border: 5px solid black; }

Actual width becomes:
200 + 20 + 20 + 5 + 5 = 250px

🔹 border-box (Recommended)
.box { box-sizing: border-box; }

Now:
Total width = 200px (including padding & border)

## 🎯 7️⃣ Create Card Layout
## HTML :
<!DOCTYPE html>
<html>
<head>
    <title>Week 5 - CSS Box Model</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1 class="main-heading">My Card Section</h1>

    <div class="card-container">

        <div class="card">
            <h2>Card 1</h2>
            <p>This is a simple card using CSS box model properties.</p>
            <button class="btn">Read More</button>
        </div>

        <div class="card">
            <h2>Card 2</h2>
            <p>We are learning margin, padding, border and max-width.</p>
            <button class="btn">Read More</button>
        </div>

        <div class="card">
            <h2>Card 3</h2>
            <p>This layout will look clean and professional.</p>
            <button class="btn">Read More</button>
        </div>

    </div>

</body>
</html>

## CSS
 
* {
  
    margin: 0;
    padding: 0;
    box-sizing: border-box;

}

body {
   
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    padding: 40px;

}

.main-heading {
 
    text-align: center;
    margin-bottom: 40px;   

}

 
.card-container {

    max-width: 1000px;      
    margin: auto;           

}

 
.card {

    background: white;
    border: 2px solid #ddd;    
    border-radius: 10px;
    padding: 20px;               
    margin-bottom: 20px;         

}

 
.btn {

    margin-top: 15px;
    padding: 10px 15px;
    border: none;
    background-color: #007BFF;
    color: white;
    cursor: pointer;
    border-radius: 5px;

}

.btn:hover {

    background-color: #0056b3;

}


## OUTPUT
![DAY-5 OUTPUT](img/day-5-output.png)

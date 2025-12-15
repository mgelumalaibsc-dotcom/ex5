# Ex.05 Design a Website for Server Side Processing
## Date:Elumaai G
## REf.no:25016790
## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Incandescent Bulb Power Calculator</title>
    <style>
        body { font-family: Arial; text-align: center; padding: 50px; background: #f9f9f9; }
        input, button { padding: 10px; margin: 10px; font-size: 16px; }
        .result { margin-top: 20px; font-weight: bold; font-size: 20px; }
        .error { color: red; }
    </style>
</head>
<body>
    <h1>Incandescent Bulb Power Calculator</h1>
    <form method="post">
        {% csrf_token %}
        <label>Voltage (V): </label>
        <input type="text" name="voltage" value="{{ voltage }}"><br>
        <label>Current (I): </label>
        <input type="text" name="current" value="{{ current }}"><br>
        <label>Resistance (R): </label>
        <input type="text" name="resistance" value="{{ resistance }}"><br>
        <button type="submit">Calculate Power</button>
    </form>

    {% if power %}
        <div class="result">Power of the filament: {{ power|floatformat:2 }} W</div>
    {% elif error_message %}
        <div class="error">{{ error_message }}</div>
    {% endif %}
</body>
</html>

~~~


## SERVER SIDE PROCESSING:
<img width="1909" height="976" alt="Screenshot 2025-12-15 144805" src="https://github.com/user-attachments/assets/3e22996e-0720-400b-a7e8-33b555a700bf" />


## HOMEPAGE:
<img width="1591" height="750" alt="Screenshot 2025-12-15 144126" src="https://github.com/user-attachments/assets/b6684639-ea92-4885-a6e3-967c65bb04a4" />


## RESULT:
The program for performing server side processing is completed successfully.

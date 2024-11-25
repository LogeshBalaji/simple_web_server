# EX01 Developing a Simple Webserver

# Date:
## 21/11/2024
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
## urls.py(server1)  
from django.urls import path  

from.import views  

urlpatterns=[  
    path('',views.home,name='home')  
]  
## views.py(server1)  
from django.shortcuts import render    
from django.http import HttpResponse  
#Create your views here.  

def home(request):  
    return render(request, 'home.html')  
## urls.py(server)
from django.contrib import admin  
from django.urls import path,include  

urlpatterns = [  
    path('', include('server1.urls')),  
    path('admin/', admin.site.urls),  
]  
## creating new folder templates in that new html file 'home'  

content = """  
~~~
<!DOCTYPE html>    
<html lang="en">     
<head>    
  <meta charset="UTF-8">      
  <meta name="viewport" content="width=device-width, initial-scale=1.0">     
  <title>Laptop Specifications</title>    
  <style>      
    body {    
      font-family: 'Arial', sans-serif;    
      background-color: #f0f0f0;    
      color: #333;    
      display: flex;    
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      margin: 0;  
    }  

    .specs-container {
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      padding: 30px;
      width: 350px;
      text-align: center;
    }

    h1 {
      font-size: 24px;
      margin-bottom: 20px;
      color: #2c3e50;
    }

    .specs-list {
      list-style-type: none;
      padding: 0;
      margin: 0;
    }

    .specs-list li {
      background-color: #f9f9f9;
      padding: 10px;
      margin: 10px 0;
      border-radius: 4px;
      display: flex;
      justify-content: space-between;
      font-size: 16px;
      font-weight: bold;
    }

    .specs-list li span {
      color: #2980b9;
    }

    .specs-list li:nth-child(even) {
      background-color: #ecf0f1;
    }

    .footer {
      margin-top: 20px;
      font-size: 14px;
      color: #7f8c8d;
    }
  </style>
</head>
<body>

  <div class="specs-container">
    <h1>[Name:Logesh B]]</h1>
    <h1>[Reg no :24900577]</h1>
    <h1>Laptop Specifications</h1>
    <ul class="specs-list">
      <li><span>Model:</span> lenovo E16</li>
      <li><span>Processor:</span> Intel Core i5 13th Gen</li>
      <li><span>RAM:</span> 16GB DDR4</li>
      <li><span>Storage:</span> 512GB SSD</li>
      <li><span>Display:</span> 15.6" 4K UHD</li>
      <li><span>Graphics:</span> NVIDIA GeForce GTX 1650</li>
      <li><span>Battery:</span> 10 hours</li>
      <li><span>OS:</span> Windows 11</li>
    </ul>
    <div class="footer">Created with love by You!</div>
  </div>

</body>
</html>
"""

~~~

# OUTPUT:
![Screenshot 2024-11-25 132256](https://github.com/user-attachments/assets/87c595d7-dd9d-49eb-b733-5a507a93946c)

## VISUAL STUDIO CODE
![Screenshot 2024-11-21 212050](https://github.com/user-attachments/assets/5f8f826e-fb00-492f-a527-39821ea9293d)
## LAPTOP SPECIFICATIONS
![Screenshot 2024-11-21 211719](https://github.com/user-attachments/assets/b26c6166-b68a-40f3-8be9-0a2dec61c69b)




# RESULT:
The program for implementing simple webserver is executed successfully.

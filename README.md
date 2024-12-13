# ERPro Template for Django Project

## Overview
This repository contains the HTML and CSS template used for the ERPro project built on Django. The template provides a responsive and modern design, tailored for ERP applications, ensuring a seamless user experience.

### Live Demo
You can preview the template by visiting the live demo:
[Dashboard Template](https://it-corner-erp.github.io/template-erpro/html/dashboard.html)

## Features
- **Responsive Design**: Optimized for all screen sizes, including mobile, tablet, and desktop.
- **Modern UI**: Clean and intuitive design suitable for ERP systems.
- **Reusable Components**: Includes modular elements such as navigation bars, tables, forms, and charts.
- **Customizable**: Easily adaptable to specific project requirements.

## Installation

### Prerequisites
Ensure you have the following installed:
- Django framework
- A web browser for template preview

### Steps
1. Clone the repository containing the template:
   ```bash
   git clone https://github.com/it-corner-erp/template-erpro.git
   ```
2. Copy the HTML, CSS, and any associated assets (like images, JavaScript files) into your Django project's static and templates directories:
   ```
   /static
     /css
     /js
     /images

   /templates
     dashboard.html
   ```
3. Configure Django to serve the static files by updating your `settings.py`:
   ```python
   STATIC_URL = '/static/'
   STATICFILES_DIRS = [
       BASE_DIR / "static",
   ]
   ```
4. Use the template in your Django views. For example:
   ```python
   from django.shortcuts import render

   def dashboard(request):
       return render(request, 'dashboard.html')
   ```

## Usage
- **Modify Layout**: Edit `dashboard.html` and the corresponding CSS files to customize the layout and styles.
- **Integrate with Django**: Replace static content with Django template tags to dynamically render data. For example:
  ```html
  <h1>Welcome, {{ user.username }}</h1>
  ```
- **Static File Management**: Ensure all CSS and JavaScript files are loaded correctly using `{% static %}` tags.

## Contribution
If you wish to contribute to improving this template:
1. Fork the repository.
2. Make changes to the code.
3. Submit a pull request with a description of the changes made.

## License
This project is licensed under the MIT License. Feel free to use and modify it as per your requirements.

## Acknowledgments
Special thanks to the IT Corner ERP team for creating and maintaining this template. For questions or support, please contact the project maintainers.

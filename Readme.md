# Product Inventory Management System

This project is a **Product Inventory Management System** that allows users to manage a list of products. The project includes backend API development using **Django REST Framework (DRF)** and a simple frontend interface built with **HTML**, **CSS**, and **JavaScript**.

---

## Features

### Backend (Django REST Framework):
- **Model:**
  - `Product` model with fields:
    - `Name`: (CharField, max_length=100)
    - `Price`: (DecimalField)
    - `Stock`: (IntegerField)
  - Validation to ensure the price is non-negative.

- **API Endpoints:**
  - **List all products:** `GET /products/`
  - **Add a new product:** `POST /products/`
  - **Update a product:** `PUT /products/<id>/`
  - **Delete a product:** `DELETE /products/<id>/`

### Frontend:
- A responsive user interface using **Bootstrap**.
- Functionalities:
  - Add new products.
  - View the product list.
  - Edit product details.
  - Delete products.

---

## Technologies Used

### Backend:
- Python
- Django
- Django REST Framework

### Frontend:
- HTML5
- CSS3 (Bootstrap 4.5)
- JavaScript (Fetch API)

---

## Setup Instructions

### Prerequisites
- Python 3.x
- Django 4.x

### Installation

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd product-inventory
   ```

2. **Setup Virtual Environment:**
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Run the Development Server:**
   ```bash
   python manage.py runserver
   ```

6. **Access the Application:**
   Open your browser and navigate to `http://127.0.0.1:8000`.

---

## Usage Instructions

1. **Add a Product:**
   - Fill out the `Name`, `Price`, and `Stock` fields in the form and click **Add Product**.

2. **View Products:**
   - The list of products will be displayed in a table below the form.

3. **Edit a Product:**
   - Click the **Edit** button next to a product to prefill the form.
   - Make changes and click **Add Product** to save.

4. **Delete a Product:**
   - Click the **Delete** button next to a product to remove it from the list.

---

## API Documentation

### Endpoints:

#### 1. **List Products**
   - **URL:** `/products/`
   - **Method:** `GET`
   - **Response:**
     ```json
     [
         {
             "id": 1,
             "name": "Product A",
             "price": 100.0,
             "stock": 10
         }
     ]
     ```

#### 2. **Add a Product**
   - **URL:** `/products/`
   - **Method:** `POST`
   - **Request Body:**
     ```json
     {
         "name": "Product A",
         "price": 100.0,
         "stock": 10
     }
     ```
   - **Response:**
     ```json
     {
         "id": 1,
         "name": "Product A",
         "price": 100.0,
         "stock": 10
     }
     ```

#### 3. **Update a Product**

   - **URL:** `/products/<id>/`
   - **Method:** `PUT`
   - **Request Body:**
     ```json
     {
         "name": "Product A Updated",
         "price": 120.0,
         "stock": 15
     }
     ```
   - **Response:**
     ```json
     {
         "id": 1,
         "name": "Product A Updated",
         "price": 120.0,
         "stock": 15
     }
     ```

#### 4. **Delete a Product**
   - **URL:** `/products/<id>/`
   - **Method:** `DELETE`
   - **Response:** `204 No Content`

---

## Possible Enhancements
- Add user authentication.
- Include search and filter functionality for products.
- Implement pagination for product listings.
- Add unit tests and integration tests.
- Deploy the application to a cloud platform.

---




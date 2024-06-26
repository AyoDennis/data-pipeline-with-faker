# Business Data Generator

This Python script generates synthetic business-related data and stores it in a PostgreSQL database. The generated data includes patient information, order details, payment information, shipping information, medical product information, and customer support records. The script uses the `Faker` library to generate realistic fake data and `pandas` to manipulate and save it.

## Features

- Generates 100 rows of synthetic data for various business entities.
- Data types include patient details, order information, payment details, shipping information, medical products, and customer support records.
- Saves the data in a Parquet file for efficient storage.
- Loads the data into a PostgreSQL database.

## Prerequisites

- Python 3.x
- PostgreSQL database
- The following Python libraries:
  - `Faker`
  - `sqlalchemy`
  - `pandas`
  - `pyarrow`

## Setup

### Step 1: Install Python Libraries

Make sure you have Python installed. You can install the required libraries using `pip`:

```bash
pip install faker sqlalchemy pandas pyarrow
```

### Step 2: Configure PostgreSQL Database

You need to have a PostgreSQL database set up. You can use a cloud-based service like ElephantSQL or a local PostgreSQL instance. Replace the placeholder values in the `db_link` variable with your actual database connection details.

```python
db_link = "postgresql://username:password@host:port/database"
```

### Step 3: Run the Script

Run the script to generate the data and load it into your PostgreSQL database:

```bash
python business_data_generator.py
```

## How It Works

1. **Data Generation**: The script uses `Faker` to generate random but realistic data for the following entities:
    - **Patients**: Includes name, age, gender, medical history, allergies, and prescriptions.
    - **Orders**: Includes order number, date, time, items, quantity, price, and total amount.
    - **Payments**: Includes payment method, credit card number, expiration date, security code, and billing address.
    - **Shipping**: Includes recipient name, address, city, state, ZIP code, shipping method, and tracking number.
    - **Medical Products**: Includes product name, description, category, brand, price, availability, and reviews.
    - **Customer Support**: Includes support ticket number, date, time, customer name, issue description, support agent name, and resolution status.

2. **Data Storage**: The generated data is stored in a `pandas` DataFrame and saved as a Parquet file (`business_data.parquet`).

3. **Database Insertion**: The data is inserted into a PostgreSQL database table named `business_data`.

## Data Columns

The generated DataFrame includes the following columns:

- **Index**: Unique identifier for each row.
- **Patient Name**: Name of the patient.
- **Patient Age**: Age of the patient.
- **Patient Gender**: Gender of the patient.
- **Medical History**: Medical history of the patient.
- **Allergies**: Allergies of the patient.
- **Prescriptions**: Prescriptions for the patient.
- **Order Number**: Unique identifier for the order.
- **Order Date**: Date of the order.
- **Order Time**: Time of the order.
- **Order Items**: Items included in the order.
- **Order Quantity**: Quantity of items ordered.
- **Order Price**: Price of a single item.
- **Order Total Amount**: Total amount of the order.
- **Shipping Name**: Name of the recipient.
- **Shipping Address**: Address of the recipient.
- **Shipping City**: City of the recipient.
- **Shipping State**: State of the recipient.
- **Shipping ZIP Code**: ZIP code of the recipient.
- **Shipping Method**: Method of shipping.
- **Tracking Number**: Tracking number for the shipment.
- **Payment Method**: Payment method used.
- **Credit Card Number**: Credit card number used for payment.
- **Expiration Date**: Expiration date of the credit card.
- **Security Code**: Security code of the credit card.
- **Billing Address**: Billing address.
- **Product Name**: Name of the medical product.
- **Product Description**: Description of the medical product.
- **Product Category**: Category of the medical product.
- **Product Brand**: Brand of the medical product.
- **Product Price**: Price of the medical product.
- **Product Availability**: Availability status of the product.
- **Product Reviews**: Number of reviews for the product.
- **Support Ticket Number**: Unique identifier for the support ticket.
- **Support Date**: Date of the support request.
- **Support Time**: Time of the support request.
- **Customer Name**: Name of the customer requesting support.
- **Issue Description**: Description of the issue.
- **Support Agent Name**: Name of the support agent handling the ticket.
- **Resolution Status**: Resolution status of the ticket.

## Contribution

Feel free to fork this repository and submit pull requests. For major changes, please open an issue to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact

For any questions or support, please open an issue on GitHub or contact the maintainer at [ayodejidennis33@gmail.com].


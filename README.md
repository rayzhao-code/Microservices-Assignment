# Microservices Architecture Assignment

Two Flask services:
- **User Service** (port 5001) provides endpoints to create and retrieve users and stores user data in a simple in-memory dictionary.
- **Order Service** (port 5002) provides endpoints to create and retrieve orders.

## Setup
```bash
# Create a virtual environment
python -m venv myenv

# Activate the virtual environment
source myenv/bin/activate      # Windows: myenv\bin\activate

# Install Flask
pip install flask
pip install requests
```

## Running the Services
### Start the User Service
```bash
python user_service.py
```
![](screenshots/ss1.png)

### Start the Order Service
```bash
python order_service.py
```
![](screenshots/ss2.png)

## Example Requests

### Create a User
```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"Ray", "email": "ray@example.com"}' http://localhost:5001/users
```
![](screenshots/ss3.png)

### Get a User
```bash
curl http://localhost:5001/users/3
```
![](screenshots/ss4.png)

### Create an Order
```bash
curl -X POST -H "Content-Type: application/json" -d '{"user_id":3, "product": "Tablet"}' http://localhost:5002/orders
```
![](screenshots/ss5.png)

### Get an Order
```bash
curl http://localhost:5002/orders/3
```
![](screenshots/ss6.png)

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
![](screenshots/ss1.png)

### Start the Order Service
![](screenshots/ss2.png)

## Example Requests

### Create a User
![](screenshots/ss3.png)

### Get a User
![](screenshots/ss4.png)

### Create an Order
![](screenshots/ss5.png)

### Get an Order
![](screenshots/ss6.png)

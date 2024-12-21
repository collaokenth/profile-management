# profile-management
extract zip 
open vscode
open folder
select the extracted file
open terminal

# installl this on terminal
pip install flask
pip install mysql.connector
pip install flask_bcrypt
pip install flask_login

# run the code
click "http://127.0.0.1:5000"

# note make sure to create a database
# database name
profile_management

# database table 
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE profiles (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    date_of_birth DATE NOT NULL,
    user_id INT NOT NULL,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE
);



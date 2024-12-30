# BookShopWeb

A Java Web project to build an online Bookstore  
![Catalog](https://user-images.githubusercontent.com/60851390/228592444-282493ee-7ebd-4115-b40f-af23ec7dfa08.png)

| (1)                                                                                          | (2)                                                                                          | (3)                                                                                          |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| <img src="https://user-images.githubusercontent.com/60851390/228592577-87976ca7-76c6-44c8-ab18-e664cce7493d.png" alt="Home" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592589-fa4302d4-a82e-4697-b22a-f84115885946.png" alt="Signup" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592594-fb3cec7c-7aac-47a4-8c4b-33a8792a2578.png" alt="Signin" width="200" /> |
| <img src="https://user-images.githubusercontent.com/60851390/228592602-8fe8fc00-89cb-4bc4-bb4b-b6c4e172dcfd.png" alt="Category" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592605-cf258cf4-3afe-4814-b649-2e5cfa3dc7f2.png" alt="Product" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592610-afc17126-f5da-45a2-b0b6-c4b89e39bf35.png" alt="Cart" width="200" /> |
| <img src="https://user-images.githubusercontent.com/60851390/228592611-c41f8048-48fc-45a4-82db-91e8f4dcc808.png" alt="User" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592615-1785a568-bc06-4556-a53b-3253dd782945.png" alt="Order" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592619-eb6d56ba-49ba-461a-9616-83926d3e794c.png" alt="Order Detail" width="200" /> |
| <img src="https://user-images.githubusercontent.com/60851390/228592622-47b20682-7314-4033-b35f-232630d2cf4b.png" alt="Wishlist" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592628-be226989-3b7d-4bca-9d8a-1cdfc60b6aca.png" alt="Search" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592633-fe3bc1c0-bfc8-4600-9cae-2038221bba9d.png" alt="Edit Review" width="200" /> |
| <img src="https://user-images.githubusercontent.com/60851390/228592634-df36905e-e377-442e-82f1-89eb5c921960.png" alt="Admin Dashboard" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592637-09d61699-6f0e-404b-b32b-e969ab864e78.png" alt="Product Management" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592639-3cc4767f-ce03-4521-a7de-9f993d4cbe2c.png" alt="Create Product" width="200" /> |
| <img src="https://user-images.githubusercontent.com/60851390/228592645-0ffedb14-78d6-47c2-9577-59a802159251.png" alt="Update Product" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592649-c7325684-cf12-406d-9fc7-b4980b668c7d.png" alt="Review Management" width="200" /> | <img src="https://user-images.githubusercontent.com/60851390/228592653-99341b4d-f200-4890-b556-a59bccefb789.png" alt="Order Management" width="200" /> |

## A. Set up the BookShopWeb project

### 1. Load images

Create the directory `C:/var/webapp/images` and extract all images from the file [var-webapp-images.zip](https://github.com/hoangquan2002/BookShopManagement/blob/main/init/var-webapp-images.zip) into this folder.

### 2. Create the database

Open MySQL Workbench → Open SQL Script → Execute [bookshopdb.sql](https://github.com/hoangquan2002/BookShopManagement/blob/main/init/bookshopdb.sql).

### 3. Load the project into IDEA

Open IntelliJ IDEA → Get from VCS (on the Welcome screen) or File | New | Project from Version Control (in the main screen) → Clone project using the URL: https://github.com/hoangquan2002/BookShopManagement.git.

### 4. Configure Tomcat

- Go to [Add Configuration...] → [+] Tomcat Server Local.  
- Click [Fix] → Select `BookShopWeb:war exploded`.

### 5. Run (Shift+F10)

## B. Configure `utils.ConstantUtils`

- Default values: `DB_NAME` is `bookshopdb`, `DB_USERNAME` is `root`, and `DB_PASSWORD` is `12345`.  
- These can be changed if different credentials are used.

# Database Design

![DatabaseDesignBSW](https://user-images.githubusercontent.com/60851390/184755435-bb97a62a-4cdd-408d-9a5a-526430f50c64.svg)

## Sample Data

| Table            | Number of sample records |
| ----------------- | ------------------------ |
| user             | 5                        |
| product          | 100                      |
| product_review   | 150                      |
| category         | 15                       |
| product_category | 100                      |
| cart             | 2                        |
| cart_item        | 5                        |
| orders           | 25                       |
| order_item       | 60                       |
| wishlist_item    | 30                       |

# Software Used

- IntelliJ IDEA 2022.1.2  
- MySQL Workbench 8.0.25  
- Tomcat 9.0.48  

## Installing Tomcat 9.0.48

- Download from: https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.48/bin/ (`apache-tomcat-9.0.48.zip` for Windows and `apache-tomcat-9.0.48.tar.gz` for Mac).  
- Open IntelliJ IDEA and add it via File | Settings | Build, Execution, Deployment | Application Servers > [+] Tomcat Server (set Tomcat Home to the Tomcat directory, e.g., `apache-tomcat-9.0.48`).
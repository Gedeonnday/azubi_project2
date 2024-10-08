azubi_project2

About The Project Task 1: Manual Dynamo Table

We created a guestbook table. This allowed us to record data of people who visit our application. We will setup fields such as name, email and country.

🏗️ Our Default Dynamo Table Go to your AWS Console and navigate to the DynamoDB service.

Click on the "Create table" button.

Enter "GuestBook" as the table name.

Enter "Email" as the primary key and make sure to select "String" as the data type.

Create a Country and Name Fields. You may need to research on (global and local indexes)

Click on the "Create" button to create the table.

Once the table is created, click on the "Items" tab to add some sample data to the table.

Click on the "Create item" button and enter the sample data for the "Name", "Email", and "Country" fields.

Populate this with your team members info.

✨ Creating custom tables Your data should have more than 2 fields. E.g usertable (name, phone, gender)

Ensure you follow dynamo dB best practices:

Primary key, sort key

This is not compulsory, You can still use the Guestbook example above.

Task 2: Link Dynamo to webpage we will be using the AWS SDK to be able to communicate with dynamo from our webpage. We will have an extra guestlist webpage to be attached to our project

📂 Project Files Teams are encouraged to continue with their project 1 web app. the shared repo is just for clarification.

We will be working with a new page Guestlist.php we will use php as it can process the requests in the background. Pick the template for this new file here.

There are some packages needed for us to run the connection to dynamo

🏗️ Working with AWS SDK for php Install Composer (https://getcomposer.org/), a package manager for PHP.

In your project directory, run the “composer require aws/aws-sdk-php". This will install the needed packages.

Git error: Install git from here, https://git-scm.com/download

Once the AWS SDK for PHP is installed, you can use it in your PHP code by including the Composer-generated autoloader:

require 'vendor/autoload.php';

You are now able to call on dynamo and perform the desired functions.

Task 3: Using Terraform To reduce redundancy and complexities we will use terraform to create our dynamo dB table.

📂 To note A terraform file is a configuration file that defines the infrastructure and resources to be created by Terraform.

A dynamo dB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.

🏗️ Using Terraform to create dynamo dB Install Terraform on your local machine following the installation guide for your operating system: install terraform

Set up your AWS credentials on your local machine. You can do this by configuring the AWS Command Line Interface (CLI) using the aws configure command.

Create a new directory/folder on your local machine where you will store your Terraform configuration files.

Create a new file in your Terraform directory called anything.tf.

In your anything.tf file, define your AWS provider. This tells Terraform which AWS region to use and which AWS credentials to use.

To create a dynamo dB using a terraform file, you need to:

Define the attributes and settings of the dynamo dB table, such as name, hash key, range key, read capacity, write capacity, etc.

Dummy Data can be added in the same file, different file. But make sure you add the data using terraform.

Run terraform init to initialize the working directory and download the required plugins

Run terraform plan to preview the changes that will be made

Run terraform apply to create the dynamo dB table

Task 4: Deployment We will work on packaging our application

📂 Docker Hub Deployment Create a Dockerfile in the "version3" folder with the following contents: Dockerfiles are what tell docker how it should build your image (environments)

Build the Docker image using the following command:

docker build -t your-dockerhub-username/docker-web-app:3.0 .

This will build a Docker image with the name "your-dockerhub-username/docker-web-app" and the tag "3.0".

Push the Docker image to DockerHub using the following command:

docker push your-dockerhub-username/docker-web-app:3

Collaborations

This is a hand-on cloud engineering project delivered by the azubi africa cloud team in 2023. After 6 months of AWS cloud training and front-end development, we got a chance to work on some realife cloud projects. I was able to work with:

Elias Ibisi / https://www.linkedin.com/in/elias-ibisi-007914124 Ngoako Titus Rakau / https://www.linkedin.com/in/ngoako-titus-rakau Ruben Jerzy Homadzi / https://www.linkedin.com/in/ruben-jerzy-688b4569 Regina Tenkorang / https://www.linkedin.com/in/regina-tenkorang Ebenezer Ezekiel Darmoe / https://www.linkedin.com/in/ebenezer-ezekiel-darmoe-62221464 Isaac Aidoo Godwin Dorglo Dorglo

Contact Gedeon Ndayiringiye @gedeonnday ndagedeous@gmail.com

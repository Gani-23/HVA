# MERN Application Documentation

This documentation provides instructions for deploying a MERN (MongoDB, Express.js, React.js, Node.js) application on an AWS instance with Nginx routing. The frontend will be served on port 3000, while the backend will be served on port 3001. Additionally, we will configure an Application Load Balancer with a DNS name hosted on Cloudflare using a CNAME record.

## Prerequisites
- AWS account
- Cloudflare account
- Domain name

## Step 1: Launch AWS Instance
1. Log in to your AWS account.
2. Navigate to the EC2 service.
3. Launch a new instance, selecting an appropriate AMI and instance type.
4. Configure security groups to allow inbound traffic on ports 3000 and 3001.

## Step 2: Install and Configure Nginx
1. SSH into the AWS instance.
2. Install Nginx using the package manager of your choice.
3. Configure Nginx to proxy requests to the backend server running on port 3001.
4. Configure Nginx to serve the frontend files from the appropriate directory.

## Step 3: Deploy Backend Server
1. Clone your backend repository onto the AWS instance.
2. Install the required dependencies using a package manager.
3. Build and start the backend server using the appropriate commands.

## Step 4: Deploy Frontend Application
1. Clone your frontend repository onto the AWS instance.
2. Install the required dependencies using a package manager.
3. Build the frontend application using the appropriate commands.
4. Copy the built files to the directory configured in Nginx.

## Step 5: Configure Cloudflare DNS
1. Log in to your Cloudflare account.
2. Navigate to the DNS settings for your domain.
3. Add a CNAME record pointing to the DNS name of your AWS Application Load Balancer.

## Step 6: Configure AWS Application Load Balancer
1. Navigate to the EC2 service in your AWS account.
2. Create a new Application Load Balancer.
3. Configure the load balancer to listen on ports 80 and 443.
4. Add the instances running your MERN application to the target group.
5. Obtain the DNS name of the load balancer.

## Step 7: Test and Verify
1. Access your MERN application using the DNS name of the AWS Application Load Balancer.
2. Verify that the frontend is served on port 3000 and the backend on port 3001.
3. Test the functionality of your application to ensure it is working as expected.

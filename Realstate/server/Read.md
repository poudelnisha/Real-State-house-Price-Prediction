Here,is a stepwise tutorial on how to deploy the machine learning model on Amazon  EC2 instance .

1. Login to AWS, create an EC2 instance.
2. Configure security group name and add rules for HTTP and HTTPs. This would allow user from outside to make a HTTP request. 
3. Create a key pair. It ill be created as a "bem" file (amazon way of authenticating). This bem file should be saved on .ssh directory inside 
out local machine for future reference and use.It will be used to connect with AWS cloud.
4. Launch Instance.(In AWS)
5.  Now, in our local machine run git bash. Connect to EC2 instance in AWS cloud using .ssh and the user@publicdns. For example : ssh -i "C:\Users\pp\.ssh\hh_price.pem" ubuntu@ec2-3-94-90-000.compute-1.amazonaws.com
(we can get the instructions by clicking connect tab, after chosing the instance we have launched).
6. After getting connected to cloud, transfer the code by using winscp or filezella. (Use the server name given in instance connect instruction as a server).
7. Now, we can install nginx web server in our cloud ubuntu.
8. Disable the default html file of nginx in a sites-enabled directory with our real_staehome price page. We here set up a reverse proxy by writing a script for .conf file.
    server {  
    listen 80;  
        server_name bhp;  
        root /home/ubuntu/real_state/client;  
        index app.html;  
        location /api/ {  
             rewrite ^/api(.*) $1 break;  
             proxy_pass http://127.0.0.1:5000;  
             }  
        }    
        
 9. In order for our webpage to be fully functional, our python flask server should run. Install all the necessary packages on the ubuntu home page and run server.py file on local host.        
        
         
    

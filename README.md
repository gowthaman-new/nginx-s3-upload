# nginx-s3-upload
Upload file to S3 through Nginx Web Server

Installation

Create a .env file to hold your environment variables for Nginx. You can base on the .env.example file contained in root folder.

Using Docker, build the image.

$ docker build -t image-nam .
After the image is built, create a container.

$ docker run -d -p 80:80 --env-file=.env image-name
Usage

Once the container is running, give it a try!

$ curl -T path/to/file/to/upload http://yourdomainname.com/uploads/entity/property/filename.extension
The response will contain a header, X-File-URL, with the location of the file on your S3 bucket.
"yourdomainname" can be added after Load Balancer.

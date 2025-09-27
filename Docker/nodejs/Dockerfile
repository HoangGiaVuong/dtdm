FROM node:latest

# Install git
RUN apt-get update && apt-get install -y git

WORKDIR /home/myweb

# Clone the repository (replace with your actual repo URL)
RUN git clone https://github.com/HoangGiaVuong/dtdm.git .

# Install dependencies
RUN npm install

COPY wait-for-it.sh /wait-for-it.sh
RUN chmod +x /wait-for-it.sh

EXPOSE 8080

# Use wait-for-it before starting the app
CMD ["/wait-for-it.sh", "mysql:3306", "--", "npm", "start"]
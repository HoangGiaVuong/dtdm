FROM node:latest

# Install git
RUN apt-get update && apt-get install -y git

WORKDIR /home/myweb

# Clone the repository (replace with your actual repo URL)
RUN git clone https://github.com/HoangGiaVuong/dtdm.git .

# Install dependencies
RUN npm install

# Expose ports
EXPOSE 8080

# Start the application
CMD ["npm", "start"]
FROM node
EXPOSE 5000
WORKDIR /usr/src/app

# Copy content
COPY . /usr/src/app

# Install serve
RUN npm install -g serve

# Install dependencies
RUN npm install

# Build static files
RUN npm run build

# Run the application
CMD ["serve", "-s", "-l", "5000", "build"]

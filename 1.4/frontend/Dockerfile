FROM node
EXPOSE 5000
WORKDIR /usr/src/app

# Copy content
COPY . /usr/src/app

# ENV Port if it's not default
ENV REACT_APP_BACKEND_URL=http://localhost:8080
RUN apt-get update && apt-get install -y curl

# Install serve
RUN npm install -g serve

# Install dependencies
RUN npm install

# Build static files
RUN npm run build

# Run the application
CMD ["serve", "-s", "-l", "5000", "build"]

# NodeJS version
FROM node:16

WORKDIR /dmx

COPY package*.json ./
# Put any command used to install
RUN npm install

COPY . .
# Provide the token
ENV TOKEN=$TOKEN

EXPOSE 8080
# Locally is recommended to use CMD [ "yarn", "start" ].
# Make sure only the dist file is imported into the server and not the src file. 
CMD [ "node" , "." ]

FROM node:16
LABEL project="angular"
LABEL author="sufiyan"
RUN git clone https://github.com/instinct1one/angular-realworld-example-app.git
RUN cd angular-realworld-example-app
RUN npm install -g @angular/cli && \
    npm install --global --force yarn && \
    npm install && \
    yarn install
EXPOSE 4200
WORKDIR /angular-realworld-example-app
CMD ["ng", " build --prod", "serve", "--host", "0.0.0.0"]


######
FROM node:16
LABEL project="angular"
LABEL author="sufiyan"
RUN git clone https://github.com/gothinkster/angular-realworld-example-app.git
RUN cd angular-realworld-example-app && npm install -g @angular/cli && npm install
EXPOSE 4200
WORKDIR /angular-realworld-example-app
CMD ["ng", "serve", "--host", "0.0.0.0"]
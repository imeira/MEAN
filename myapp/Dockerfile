FROM node
RUN apt-get update -q && apt-get dist-upgrade -y && apt-get clean && apt-get autoclean
EXPOSE 3000
ENV APP_PATH /c/Users/meira/OneDrive/IdeaProjects/MEAN/myapp
RUN mkdir -p $APP_PATH && chown node:node $APP_PATH && chmod -R 777 $APP_PATH
WORKDIR $APP_PATH
USER root
COPY . $APP_PATH/
RUN npm install
CMD ["npm","start"]

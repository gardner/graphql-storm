FROM node:carbon
EXPOSE 5000
ENV PGURL "postgresql://postgres:postgres@db:5432/postgres"

RUN npm install -g postgraphile

CMD postgraphile -n 0.0.0.0 -c $PGURL --schema forum_example --watch --enhance-graphiql 

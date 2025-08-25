FROM node:24-alpine3.22

RUN addgroup app && adduser -S -G app app
USER app

WORKDIR /app

COPY --chown=app:app package*.json .
RUN npm install
COPY --chown=app:app . .

# CMD npm start - this is shell form; prefer exec form
# CMD ["npm", "start"] - this and ENTRYPOINT do the same thing; prefer ENTRYPOINT
ENTRYPOINT ["npm", "start"]

ENV MY_API=test-api
EXPOSE 3000

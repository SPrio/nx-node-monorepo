# This file is generated by Nx.
#
# Build the docker image with `npx nx docker-build app-1`.
# Tip: Modify "docker-build" options in project.json to change docker build args.
#
# Run the container with `docker run -p 3000:3000 -t app-1`.
FROM docker.io/node:lts-alpine

ENV HOST=0.0.0.0
ENV PORT=3000

WORKDIR /app

RUN addgroup --system app-1 && \
          adduser --system -G app-1 app-1

COPY dist/apps/app-1 app-1
RUN chown -R app-1:app-1 .

# You can remove this install step if you build with `--bundle` option.
# The bundled output will include external dependencies.
RUN npm --prefix app-1 --omit=dev -f install

CMD [ "node", "app-1" ]

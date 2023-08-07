FROM nginx:mainline-alpine

# Set the working directory to /app
WORKDIR /app

# Expose port 8080 to the host
EXPOSE 8080

HEALTHCHECK --interval=5s --timeout=3s \
  CMD curl -f http://localhost/ || exit 1


ONBUILD RUN echo "You are using this as a based image"

VOLUME /jorge

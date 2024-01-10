FROM openjdk:22-ea-29
ARG FILE_NAME
RUN addgroup boot
RUN adduser -D -h /home/boot -s /bin/ash boot -G boot
USER boot
WORKDIR /home/boot
ADD ./backend/target/$FILE_NAME.jar devops.jar
EXPOSE 8080
CMD java -jar devops.jar
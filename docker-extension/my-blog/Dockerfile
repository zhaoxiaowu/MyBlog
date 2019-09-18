FROM java:8
VOLUME /tmp
ADD *.jar app.jar
#解决Docker时区和宿主不一致
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN bash -c 'touch /app.jar'
CMD nohup java -jar /app.jar --spring.profiles.active=docker
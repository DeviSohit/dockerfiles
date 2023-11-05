FROM almalinux:8
# if i keep frequent changing instuction, it will change all layers so that iam keeping at end
# RUN echo "Hello World"
RUN yum install nginx -y
RUN echo "Hello, Welcome to Dockerfile. A way of creating own images" > /usr/share/nginx/html/hello.html
# provisioning layesr to save memory storage..running 3 instructions in 1 layer. 1 instruction will be 1 layer
RUN yum install git -y \
    && yum install maven -y \
    && yum install gcc -y
# keeping frequent changing instuction at end to not get changes in all layers(provisioning layers)
RUN echo "Hell Docker"
CMD [ "nginx", "-g", "daemon off;" ]
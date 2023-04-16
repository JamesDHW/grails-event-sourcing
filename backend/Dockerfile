FROM amazoncorretto:8

ENV GRAILS_VERSION 3.3.2
ENV GROOVY_VERSION 2.4.13
ENV GRADLE_VERSION 3.5.1

RUN yum update -y && yum install -y curl zip unzip

# Install sdkman tool: https://docs.grails.org/3.3.2/guide/single.html#requirements
RUN curl -s "https://get.sdkman.io" | bash
RUN /bin/bash -c "source /root/.sdkman/bin/sdkman-init.sh && \
    sdk install grails $GRAILS_VERSION && \
    sdk install groovy $GROOVY_VERSION && \
    sdk install gradle $GRADLE_VERSION"

CMD ["bash"]


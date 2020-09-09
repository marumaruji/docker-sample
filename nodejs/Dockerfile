FROM amazonlinux:2.0.20200406.0

LABEL maintainer="marumaruji"

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
  && yum -y install unzip \
  && unzip awscliv2.zip \
  && ./aws/install \
  && rm -r awscliv2.zip \
  && rm -rf aws \
  && curl --silent --location https://rpm.nodesource.com/setup_12.x | bash - \
  && yum -y install nodejs \
  && yum -y install groff-base git procps \
  && mkdir /opt/src \
  && mkdir /root/.aws \
  && npm install -g @nestjs/cli nodemon

EXPOSE 3000

WORKDIR /opt/src
# docker-compose run --rm --service-ports nestjs
FROM nginx

RUN apt-get update && apt-get -y install ssh && apt-get install -y git

ARG GITHUB_SSH_KEY=C:\Users\tsantora\.ssh\id_rsa

RUN mkdir /root/.ssh/

RUN echo "${GITHUB_SSH_KEY}" > /root/.ssh/known_hosts

# make sure your domain is accepted
RUN touch /root/.ssh/known_hosts
RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

RUN git clone git@github.com:git/DPRMC/FIMS.git







